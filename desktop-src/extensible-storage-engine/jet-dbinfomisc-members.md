---
description: 'En savoir plus sur les membres suivants : JET_DBINFOMISC'
title: Membres JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc_members(v=EXCHG.10)
ms:contentKeyID: 39515834
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 50028b810184b9562a4175e50e72d0ac8cb2ba1e61c76c134ba2c1fbcd4e7533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968419"
---
# <a name="jet_dbinfomisc-members"></a>Membres JET_DBINFOMISC

Inclure les membres protégés  
Inclure les membres hérités  

Contient diverses informations sur une base de données. Il s’agit des informations contenues dans l’en-tête de base de données.

Le type de [JET_DBINFOMISC](./jet-dbinfomisc-class.md) expose les membres suivants.

## <a name="constructors"></a>Constructeurs

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh566519(v=exchg.10).md">JET_DBINFOMISC</a></td>
<td></td>
</tr>
</tbody>
</table>


Haut

## <a name="properties"></a>Propriétés

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh578821(v=exchg.10).md">bkinfoCopyPrev</a></td>
<td>Obtient des informations sur la dernière sauvegarde de copie réussie.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh565264(v=exchg.10).md">bkinfoDiffPrev</a></td>
<td>Obtient des informations sur la dernière sauvegarde différentielle réussie. Réinitialisez lorsque <a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a> est défini.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh577657(v=exchg.10).md">bkinfoFullCur</a></td>
<td>Obtient des informations sur la sauvegarde actuelle.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a></td>
<td>Obtient des informations sur la dernière sauvegarde complète réussie.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh564433(v=exchg.10).md">bkinfoIncPrev</a></td>
<td>Obtient des informations sur la dernière sauvegarde incrémentielle réussie. Cette valeur est réinitialisée lorsque <a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a> est défini.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh578850(v=exchg.10).md">cbPageSize</a></td>
<td>Obtient la taille de la page de la base de données. La valeur 0 correspond à 4 Ko de pages.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh558061(v=exchg.10).md">dbstate</a></td>
<td>Obtient l’état cohérent/incohérent de la base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh566598(v=exchg.10).md">dwBuildNumber</a></td>
<td>Obtient le numéro de build du système d’exploitation à partir du dernier attachement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh578966(v=exchg.10).md">dwMajorVersion</a></td>
<td>Obtient la version principale du système d’exploitation à partir du dernier attachement.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh596571(v=exchg.10).md">dwMinorVersion</a></td>
<td>Obtient la version mineure du système d’exploitation à partir du dernier attachement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh564660(v=exchg.10).md">fShadowingDisabled</a></td>
<td>Obtient une valeur qui indique si l’occultation de catalogue est activée. Cette valeur est réservée à un usage interne uniquement.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh565757(v=exchg.10).md">fUpgradeDb</a></td>
<td>Obtient une valeur indiquant si la base de données est en cours de mise à niveau. Cette valeur est réservée à un usage interne uniquement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh579055(v=exchg.10).md">genCommitted</a></td>
<td>Obtient la génération de journal maximale validée dans la base de données. En général, génération de journal en cours.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh579109(v=exchg.10).md">genMaxRequired</a></td>
<td>Obtient la génération de journal maximale requise pour relire les journaux.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh565891(v=exchg.10).md">genMinRequired</a></td>
<td>Obtient la génération de journal minimale requise pour relire les journaux. En général, la génération du point de contrôle.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh577443(v=exchg.10).md">lgposAttach</a></td>
<td>Obtient le lgpos du dernier attachement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh163307(v=exchg.10).md">lgposConsistent</a></td>
<td>Obtient le lgpos lorsque la base de données a été rendue cohérente. Cette valeur est null si la base de données est incohérente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh566733(v=exchg.10).md">lgposDetach</a></td>
<td>Obtient le lgpos du dernier détachement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh564456(v=exchg.10).md">logtimeAttach</a></td>
<td>Obtient l’heure à laquelle la base de données a été attachée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh566711(v=exchg.10).md">logtimeBadChecksum</a></td>
<td>Obtient la dernière heure à laquelle une erreur de somme de contrôle non corrigeable a été trouvée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh557946(v=exchg.10).md">logtimeConsistent</a></td>
<td>Obtient l’heure à laquelle la base de données a été rendue cohérente. Cette valeur est null si la base de données est incohérente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh556940(v=exchg.10).md">logtimeDetach</a></td>
<td>Obtient l’heure du dernier détachement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh557356(v=exchg.10).md">logtimeECCFixFail</a></td>
<td>Obtient la dernière fois qu’une erreur incorrecte de bit s’est produite.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh578967(v=exchg.10).md">logtimeECCFixSuccess</a></td>
<td>Obtient la dernière fois qu’une erreur d’un bit a été résolue avec succès.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh577625(v=exchg.10).md">logtimeGenMaxCreate</a></td>
<td>Obtient l’heure de création du fichier journal <a href="hh579109(v=exchg.10).md">genMaxRequired</a> .</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh579510(v=exchg.10).md">logtimeRepair</a></td>
<td>Obtient l’heure de la dernière exécution de la réparation sur cette base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh565142(v=exchg.10).md">lSPNumber</a></td>
<td>Obtient le numéro du Service Pack du système d’exploitation à partir du dernier attachement.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh564996(v=exchg.10).md">signDb</a></td>
<td>Obtient la signature de la base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh578351(v=exchg.10).md">signLog</a></td>
<td>Obtient la signature du fichier journal des journaux utilisés pour modifier la base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh596347(v=exchg.10).md">ulBadChecksum</a></td>
<td>Obtient le nombre de fois qu’une erreur de somme de contrôle non corrigeable a été détectée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh557876(v=exchg.10).md">ulBadChecksumOld</a></td>
<td>Obtient le nombre de fois qu’une erreur de somme de contrôle non réparable a été détectée avant la dernière réparation.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh566254(v=exchg.10).md">ulECCFixFail</a></td>
<td>Obtient le nombre de fois où une erreur d’un bit non corrigeable a été rencontrée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh564490(v=exchg.10).md">ulECCFixFailOld</a></td>
<td>Obtient le nombre de fois où une erreur d’un bit non corrigeable a été rencontrée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh578574(v=exchg.10).md">ulECCFixSuccess</a></td>
<td>Obtient le nombre de fois qu’une erreur d’un bit a été corrigée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh578638(v=exchg.10).md">ulECCFixSuccessOld</a></td>
<td>Obtient le nombre de fois qu’une erreur d’un bit a été corrigée correctement avant la dernière réparation.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh579357(v=exchg.10).md">ulRepairCount</a></td>
<td>Obtient le nombre de fois que la réparation a été appelée sur cette base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh557020(v=exchg.10).md">ulRepairCountOld</a></td>
<td>Obtient le nombre de fois que cette base de données a été réparée avant la dernière défragmentation.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh596219(v=exchg.10).md">ulUpdate</a></td>
<td>Obtient la version incrémentielle d’esent qui a créé la base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh577854(v=exchg.10).md">ulVersion</a></td>
<td>Obtient la version de esent qui a créé la base de données.</td>
</tr>
</tbody>
</table>


Haut

## <a name="methods"></a>Méthodes

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh557934(v=exchg.10).md">Égal à (objet)</a></td>
<td>Détermine si l' <a href="/dotnet/api/system.object">objet</a> spécifié est égal à l' <a href="/dotnet/api/system.object">objet</a>actuel. (Substitue <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object. Equals (Object)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh565657(v=exchg.10).md">Égal à (JET_DBINFOMISC)</a></td>
<td>Indique si l'objet actuel est égal à un autre objet du même type.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh558400(v=exchg.10).md">GetHashCode</a></td>
<td>Retourne le code de hachage de cette instance. (Substitue <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object. GetHashCode ()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh556970(v=exchg.10).md">ToString</a></td>
<td>Obtient une représentation sous forme de chaîne de cet objet. (Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_DBINFOMISC](./jet-dbinfomisc-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
