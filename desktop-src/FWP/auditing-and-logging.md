---
title: Audit
description: La plateforme de filtrage Windows (WFP) permet d’auditer les événements liés aux pare-feu et IPsec.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "103941533"
---
# <a name="auditing"></a>Audit

La plateforme de filtrage Windows (WFP) permet d’auditer les événements liés au pare-feu et à IPsec. Ces événements sont stockés dans le journal de sécurité système.

Les événements audités sont les suivants :



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Catégorie d’audit</th>
<th>Sous-catégorie d’audit</th>
<th>Événements audités</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Modification de stratégie<br/> {6997984D-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtrage de la modification de stratégie de plateforme<br/> {0CCE9233-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Les nombres représentent les ID d’événements tels qu’ils sont affichés par observateur d’événements (eventvwr.exe).
</blockquote>
<br/> Ajout et suppression d’objets WFP :<br/>
<ul>
<li>légende persistante 5440 ajoutée</li>
<li>5441-temps de démarrage ou filtre persistant ajouté</li>
<li>5442 fournisseur persistant ajouté</li>
<li>5443 contexte du fournisseur persistant ajouté</li>
<li>5444 sous-couche persistante ajoutée</li>
<li>5446 ajout ou suppression d’un appel au moment de l’exécution</li>
<li>5447 filtre au moment de l’exécution ajouté ou supprimé</li>
<li>5448 fournisseur d’exécution ajouté ou supprimé</li>
<li>5449 contexte du fournisseur au moment de l’exécution ajouté ou supprimé</li>
<li>sous-couche d’exécution 5450 ajoutée ou supprimée</li>
</ul></td>
</tr>
<tr class="even">
<td>Accès aux objets<br/> {6997984A-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtrage de la suppression de paquets de plateforme <br/> {0CCE9225-69AE-11D9-BED3-505054503030}<br/></td>
<td>Paquets supprimés par WFP :<br/>
<ul>
<li>paquet 5152 abandonné</li>
<li>5153 paquet refusé</li>
</ul></td>
</tr>
<tr class="odd">
<td>Accès aux objets<br/></td>
<td>Filtrage de la connexion de plateforme <br/> {0CCE9226-69AE-11D9-BED3-505054503030}<br/></td>
<td>Connexions autorisées et bloquées :<br/>
<ul>
<li>5154 écoute autorisée</li>
<li>5155 écoute bloquée</li>
<li>5156 connexion autorisée</li>
<li>5157 connexion bloquée</li>
<li>5158 liaison autorisée</li>
<li>liaison 5159 bloquée</li>
</ul>
<blockquote>
[!Note]<br />
Les connexions autorisées n’auditent pas toujours l’ID du filtre associé. Le FilterID pour TCP sera égal à 0, sauf si un sous-ensemble de ces conditions de filtrage est utilisé : UserID, AppID, Protocol, port distant.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Accès aux objets<br/></td>
<td>Autres événements d’accès aux objets<br/> {0CCE9227-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Cette sous-catégorie active un grand nombre d’audits. Les audits spécifiques à WFP sont répertoriés ci-dessous.
</blockquote>
<br/> État de prévention du déni de service :<br/>
<ul>
<li>5148 mode de prévention DoS WFP démarré</li>
<li>5149 mode de prévention DoS WFP arrêté</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ouverture/fermeture de session<br/> {69979849-797A-11D9-BED3-505054503030}<br/></td>
<td>Mode principal IPsec<br/> {0CCE9218-69AE-11D9-BED3-505054503030}<br/></td>
<td>Négociation en mode principal IKE et AuthIP :<br/>
<ul>
<li>4650, 4651 Association de sécurité établie</li>
<li>4652, échec de la négociation 4653</li>
<li>4655 Association de sécurité terminée</li>
</ul></td>
</tr>
<tr class="even">
<td>Ouverture/fermeture de session<br/></td>
<td>Mode rapide IPsec <br/> {0CCE9219-69AE-11D9-BED3-505054503030}<br/></td>
<td>Négociation en mode rapide IKE et AuthIP :<br/>
<ul>
<li>5451 Association de sécurité établie</li>
<li>5452 Association de sécurité terminée</li>
<li>échec de la négociation 4654</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ouverture/fermeture de session <br/></td>
<td>Mode étendu IPsec<br/> {0CCE921A-69AE-11D9-BED3-505054503030}<br/></td>
<td>Négociation en mode étendu AuthIP :<br/>
<ul>
<li>4978 paquet de négociation non valide</li>
<li>4979, 4980, 4981, 4982 Association de sécurité établie</li>
<li>4983, échec de la négociation 4984</li>
</ul></td>
</tr>
<tr class="even">
<td>Système<br/> {69979848-797A-11D9-BED3-505054503030}<br/></td>
<td>Pilote IPsec<br/> {0CCE9213-69AE-11D9-BED3-505054503030}<br/></td>
<td>Paquets ignorés par le pilote IPsec :<br/>
<ul>
<li>4963 paquet de texte en clair entrant supprimé</li>
</ul></td>
</tr>
</tbody>
</table>



 

Par défaut, l’audit pour WFP est désactivé.

L’audit peut être activé par catégorie par le biais du composant logiciel enfichable MMC de l’éditeur d’objets stratégie de groupe, du composant logiciel enfichable MMC stratégie de sécurité locale ou de la commande auditpol.exe.

Par exemple, pour activer l’audit des événements de modification de stratégie, vous pouvez :

-   Utiliser l’éditeur d’objets stratégie de groupe

    1.  Exécutez **gpedit. msc**.
    2.  Développez stratégie de l’ordinateur local.
    3.  Développez Configuration de l’ordinateur.
    4.  Développez Paramètres Windows.
    5.  Développez Paramètres de sécurité.
    6.  Développez Stratégies locales.
    7.  Cliquez sur stratégie d’audit.
    8.  Double-cliquez sur auditer la modification de la stratégie pour lancer la boîte de dialogue Propriétés.
    9.  Consultez les cases à cocher réussite et échec.

-   Utiliser la stratégie de sécurité locale

    1.  Exécutez **secpol. msc**.
    2.  Développez Stratégies locales.
    3.  Cliquez sur stratégie d’audit.
    4.  Double-cliquez sur auditer la modification de la stratégie pour lancer la boîte de dialogue Propriétés.
    5.  Consultez les cases à cocher réussite et échec.

-   Utilisez la commande auditpol.exe

    -   **Auditpol/Set/Category : « modification de la stratégie »/Success : Enable/Failure : Enable**

L’audit peut être activé sur une base par sous-catégorie uniquement par le biais de la commande auditpol.exe.

Les noms de catégorie et de sous-catégorie d’audit sont localisés. Pour éviter la localisation des scripts d’audit, les GUID correspondants peuvent être utilisés à la place des noms.

Par exemple, pour activer l’audit des événements de modification de stratégie de plateforme de filtrage, vous pouvez utiliser l’une des commandes suivantes :

-   **Auditpol/Set/Subcategory : « filtrage de la stratégie de plateforme de filtrage »/Success : Enable/Failure : Enable**
-   **Auditpol/Set/Subcategory : « {0CCE9233-69AE-11D9-BED3-505054503030} »/Success : Enable/Failure : Enable**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))
</dt> <dt>

[Journal des événements](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))
</dt> <dt>

[Stratégie de groupe](/windows/deployment/deploy-whats-new)
</dt> </dl>

