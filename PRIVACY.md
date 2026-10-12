# Politique de confidentialité — Bot « Era »

**Dernière mise à jour : 12 octobre 2026**

Cette politique explique quelles données le bot Discord **Era** (ID d'application `334790539897602049`) collecte, pourquoi, combien de temps elles sont conservées, et comment exercer vos droits. L'utilisation du bot est encadrée par ses [Conditions d'utilisation](TERMS.md).

> **Champ d'application.** Era est un bot **privé et auto-hébergé**, en service depuis le 12 juillet 2017. Il fonctionne exclusivement sur le serveur Discord communautaire de **ZeratoR** et sur celui de la communauté affiliée **Mandatory**. Il n'est ni public, ni installable sur d'autres serveurs.

---

## 1. Qui est responsable du traitement ?

Le bot est développé et opéré par l'équipe technique bénévole du Discord ZeratoR (« nous »). Il tourne sur une **infrastructure privée dédiée** (cluster Kubernetes), sous notre seul contrôle. Aucune donnée n'est vendue, louée, ni transmise à des annonceurs ou à des tiers commerciaux.

**Contact :** pour toute question ou demande relative à vos données, contactez l'équipe de modération sur le serveur Discord ZeratoR : **[lien d'invitation du serveur]**. Votre demande est transmise à l'équipe technique du bot.

---

## 2. Quelles données sont collectées ?

### 2.1 Données conservées de façon persistante

| Donnée | Finalité | Où |
|---|---|---|
| **Identifiants Discord** (ID utilisateur, ID serveur, ID salon, ID message) | Faire fonctionner les rôles, sanctions et rappels | Base locale |
| **Historique des noms d'utilisateur** (20 max/personne) | Permettre aux modérateurs d'identifier une personne qui change de pseudo pour contourner une sanction | Base locale |
| **Historique des surnoms de serveur** (20 max/personne) | Idem | Base locale |
| **Date de fin de bannissement temporaire** | Lever automatiquement les bannissements à échéance | Base locale |
| **Pseudos des comptes exclus automatiquement** (500 max, dé-doublonnés) | Détecter les vagues de faux comptes/raids en repérant les pseudos similaires | Base locale |
| **Gagnants de tirages au sort** (IDs) | Éviter qu'une même personne soit tirée plusieurs fois pour le même giveaway | Base locale |
| **Rappels personnels** (ID + texte que **vous** avez saisi + heure) | Vous envoyer votre rappel quotidien en message privé | Base locale |
| **Listes MyAnimeList / configurations PC** (pseudo + lien) | Listes communautaires, **ajoutées uniquement par le staff** à la demande des membres | Base locale |

Le rôle « Membre » est attribué à partir des informations que Discord fournit déjà (date d'arrivée sur le serveur, ancienneté du compte) : le bot **ne tient aucune liste des nouveaux arrivants**.

### 2.2 Contenu des messages — traitement **transitoire**

Le bot lit le contenu des messages pour trois raisons uniquement :

1. **Appliquer les règles de certains salons** (ex. vérifier qu'un message contient bien un lien ou une image dans un salon dédié) ;
2. **Journalisation de modération** : lorsqu'un message est **modifié ou supprimé**, son contenu est **republié dans un salon privé réservé au staff** ;
3. **Reconnaître deux commandes d'administration** réservées au staff, qui s'écrivent directement dans un message.

Les slash commands et les menus contextuels ne nécessitent pas la lecture du contenu de vos messages.

Le contenu des messages n'est **jamais enregistré dans notre base de données**. Il est traité en mémoire puis abandonné. Dans le cas de la journalisation de modération, l'information **reste hébergée sur Discord** (dans un salon privé), et non chez nous.

### 2.3 Ce que nous ne collectons **pas**

- ❌ Aucune **donnée de présence** (statut en ligne, jeu en cours, écoute Spotify) — le bot n'utilise pas le *Presence Intent*.
- ❌ Aucune **adresse email**, adresse IP, donnée de localisation, ni donnée bancaire.
- ❌ Aucune **donnée sensible** au sens du RGPD (santé, opinions politiques, religieuses, orientation sexuelle, etc.).
- ❌ Aucun **profilage publicitaire**, aucune revente de données.

### 2.4 Journaux techniques

Les journaux applicatifs du bot (utilisés pour le diagnostic d'incidents) peuvent contenir des identifiants et pseudos Discord, ainsi que les actions de modération effectuées. Ils **ne contiennent pas le contenu des messages**. Ces journaux sont **internes**, à accès restreint, et purgés dans le cadre de la rotation normale des logs.

---

## 3. Sur quelle base légale ?

- **Intérêt légitime** (art. 6.1.f RGPD) : assurer la sécurité et la modération d'une communauté de plus de 10 000 membres — lutte contre les faux comptes, les raids et les comportements abusifs.
- **Consentement / exécution des règles du service** : en rejoignant le serveur, vous acceptez son **règlement**, qui vous informe que vos messages peuvent être traités à des fins de modération. Les fonctionnalités optionnelles (rappels, rôles par réaction, tirages, listes communautaires) ne sont activées **qu'à votre initiative**.

---

## 4. Combien de temps les données sont-elles conservées ?

- **Historique des noms et surnoms** : les 20 entrées les plus récentes par personne ; les plus anciennes sont automatiquement écrasées.
- **Pseudos des comptes exclus automatiquement** : 500 entrées maximum, en rotation (les plus anciennes sont supprimées).
- **Bannissements temporaires** : supprimés à l'expiration du bannissement.
- **Rappels** : conservés jusqu'à ce que vous les désactiviez avec `/reminderoff`.
- **Autres données** : conservées tant qu'elles sont nécessaires à la modération du serveur, ou jusqu'à votre demande de suppression.

Si vous quittez définitivement le serveur, vos données résiduelles peuvent être supprimées sur simple demande (voir §6).

---

## 5. Qui a accès aux données ?

- **L'équipe technique** du bot (accès à l'infrastructure), pour la maintenance.
- **Les modérateurs et administrateurs** du serveur, via les commandes du bot et les salons de logs privés — dans le cadre de leurs fonctions de modération uniquement.
- **Discord Inc.**, en tant qu'hébergeur de la plateforme, selon sa propre [politique de confidentialité](https://discord.com/privacy).

Les données ne sont **transmises à aucun autre tiers**, sauf obligation légale.

---

## 6. Vos droits

Conformément au RGPD, vous disposez d'un droit d'**accès**, de **rectification**, d'**effacement**, de **limitation** et d'**opposition** concernant vos données.

**Comment les exercer :** contactez l'équipe de modération sur le serveur Discord ZeratoR en précisant la nature de votre demande (consultation ou suppression). Les demandes sont traitées par l'équipe technique dans un délai de 30 jours maximum. La suppression est exécutée par le bot lui-même, grâce à la procédure d'effacement intégrée à Red-DiscordBot, appliquée à chacun de ses modules.

> ⚠️ **À noter :** certaines données sont indispensables à la modération. Une demande d'effacement des éléments liés à une **sanction en cours** (bannissement temporaire, historique de pseudos utilisé pour prévenir un contournement) peut être refusée au titre de notre intérêt légitime, tant que la sanction est active.

Vous pouvez également, à tout moment et sans nous contacter :

- désactiver vos rappels avec `/reminderoff` ;
- retirer vos réactions pour vous désinscrire des rôles auto-attribués.

---

## 7. Sécurité

Les données sont stockées sur un volume privé de notre cluster Kubernetes, accessible uniquement à l'équipe technique. Les identifiants d'accès du bot sont gérés hors du code source. Aucune interface publique ne permet de consulter ces données.

---

## 8. Mineurs

L'utilisation de Discord est soumise à un âge minimum (13 ans, ou plus selon votre pays). Nous ne collectons pas volontairement de données concernant des personnes en dessous de cet âge. Si vous estimez que c'est le cas, signalez-le à l'équipe de modération : les données seront supprimées.

---

## 9. Modifications

Cette politique peut évoluer avec les fonctionnalités du bot. Toute modification substantielle sera annoncée sur le serveur Discord. La date en haut de page indique la dernière mise à jour.

---