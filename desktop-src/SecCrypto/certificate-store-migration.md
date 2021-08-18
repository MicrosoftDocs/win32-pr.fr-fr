---
description: Lors de la mise à niveau d’un ordinateur ou d’une migration d’ordinateur à ordinateur, les certificats de certains magasins de certificats seront migrés.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Migration du magasin de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de694fc24433ce8db039dd677f52935da70cbf07d0a719b0871bd1e8f4b2d35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771095"
---
# <a name="certificate-store-migration"></a>Migration du magasin de certificats

Lors de la mise à niveau d’un ordinateur ou d’une migration d’ordinateur à ordinateur, les certificats de certains magasins de certificats seront migrés. Le tableau suivant répertorie les magasins de certificats qui sont migrés par défaut. pour le magasin ACRS (Automatic certificate Request Paramètres) du système, seules les [*listes de certificats de confiance*](../secgloss/c-gly.md) (ctl) sont migrées. Pour tous les autres magasins répertoriés ci-dessous, seuls les certificats sont migrés.

<table>
<thead>
<tr class="header">
<th>Système/utilisateur</th>
<th>Magasin</th>
<th>Emplacement de stockage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$ {ROWSPAN8} $System $ {REMOVE} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Racine</strong> \ <strong>Certificats</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Mes</strong> \ <strong>Certificats</strong><br/></td>

</tr>
<tr class="odd">
<td>REQUEST</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Demande</strong> \ <strong>Certificats</strong><br/></td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificats</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificats</strong><br/></td>

</tr>
<tr class="even">
<td>Interdit</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Non <strong>autorisé</strong> \ <strong>Certificats</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Autorité de certification</strong> \ <strong>Certificats</strong><br/></td>

</tr>
<tr class="even">
<td>ENREGISTREMENTS</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>ACRS</strong> \ <strong>Listes CTL</strong><br/></td>

</tr>
<tr class="odd">
<td rowspan="7">Utilisateur $ {REMOVE} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Racine</strong> \ <strong>Certificats</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td>fichier : \\ %AppData%\Microsoft\SystemCertificates\My\Certificates</td>

</tr>
<tr class="odd">
<td>REQUEST</td>
<td>fichier : \\ %AppData%\Microsoft\SystemCertificates\Request\Certificates</td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificats</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificats</strong><br/></td>

</tr>
<tr class="even">
<td>Interdit</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Non <strong>autorisé</strong> \ <strong>Certificats</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Logiciel</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Autorité de certification</strong> \ <strong>Certificats</strong><br/></td>

</tr>
</tbody>
</table>



 

Les autres magasins de certificats créés par les applications ne sont pas migrés par défaut. Les applications qui créent leurs propres magasins sont responsables de la migration des magasins qu’ils créent. Pour créer des magasins, nous vous recommandons de définir une clé de Registre dans les paramètres de l’application et de créer un magasin dans les paramètres du Registre à l’aide du fournisseur de magasin **CERT \_ Store \_ Prov \_** . Pour plus d’informations sur la migration des paramètres d’application, consultez la rubrique *comment créer un fichier de .xml personnalisé* dans le guide *utilisation d’USMT 3,0* à l’adresse [outil de migration utilisateur 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx). (Cette ressource n’est peut-être pas disponible dans certaines langues et pays ou régions.)

 

 
