---
title: Objets de groupe
description: Un groupe est représenté sous la forme d’un objet groupe dans Active Directory Domain Services.
ms.assetid: 2dd5a293-047a-4639-9c95-7074578952be
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a935d2a44d3350d8c24ca3bdb388f0a4bd8f16ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940817"
---
# <a name="group-objects"></a>Objets de groupe

Un groupe est représenté sous la forme d’un objet [**groupe**](/windows/desktop/ADSchema/c-group) dans Active Directory Domain Services. Le tableau suivant répertorie les attributs importants de l’objet de **groupe** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>cn</strong></td>
<td>Le nom commun ( <strong>CN</strong> ) est un attribut à valeur unique qui est le nom unique relatif de l’objet. Le nom <strong>commun</strong> est le nom du groupe dans Active Directory Domain Services. Comme avec tous les autres objets, le nom <strong>commun</strong> d’un groupe doit être unique parmi les objets frères dans le conteneur qui contient le groupe.<br/></td>
</tr>
<tr class="even">
<td><strong>membre</strong></td>
<td>L’attribut de <strong>membre</strong> est un attribut à valeurs multiples qui contient la liste des noms uniques des objets utilisateur, groupe et contact qui sont membres du groupe. Chaque élément de la liste est une référence liée à l’objet qui représente le membre ; par conséquent, le serveur Active Directory met automatiquement à jour les noms uniques dans la propriété de membre lorsqu’un objet membre est déplacé ou renommé.<br/></td>
</tr>
<tr class="odd">
<td><strong>groupType</strong></td>
<td>L’attribut <strong>GroupType</strong> est un attribut à valeur unique qui est un entier qui spécifie le type de groupe et l’étendue à l’aide des indicateurs binaires suivants :
<ul>
<li><strong>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_GLOBAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_UNIVERSAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong></li>
</ul>
<br/> Les trois premiers indicateurs spécifient l’étendue du groupe. L’indicateur <strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong> indique le type de groupe. Si cet indicateur est défini, le groupe est un groupe de sécurité. Si cet indicateur n’est pas défini, le groupe est un groupe de distribution. Pour plus d’informations, consultez <a href="#group-types">types de groupes</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>memberOf</strong></td>
<td>L’attribut <strong>memberOf</strong> est un attribut à valeurs multiples qui contient la liste des noms uniques des groupes qui contiennent le groupe en tant que membre. Cet attribut répertorie les groupes sous lesquels le groupe est directement imbriqué, il ne contient pas la liste récursive des prédécesseurs imbriqués. Par exemple, si le groupe D était imbriqué dans le groupe C et que le groupe b et le groupe B étaient imbriqués dans le groupe A, l’attribut <strong>memberOf</strong> du groupe D listerait les groupes C et b, mais pas le groupe a.<br/></td>
</tr>
<tr class="odd">
<td><strong>Guid</strong></td>
<td>L’attribut <strong>objectGUID</strong> est un attribut à valeur unique qui est l’identificateur unique de l’objet. Cet attribut est un identificateur global unique (GUID). Lorsqu’un objet est créé dans l’annuaire, le serveur Active Directory génère un GUID et l’assigne à l’attribut <strong>objectGUID</strong> de l’objet. Le GUID est unique au sein de l’entreprise et ailleurs.<br/> <strong>ObjectGUID</strong> est une structure de GUID 128 bits stockée en tant que OctetString.<br/></td>
</tr>
<tr class="even">
<td><strong>objectSid</strong></td>
<td>L’attribut <strong>objectSID</strong> est un attribut à valeur unique qui spécifie l’identificateur de sécurité (SID) du groupe. Le SID est une valeur unique utilisée pour identifier le groupe en tant que principal de sécurité. Il s’agit d’une valeur binaire que le système définit lors de la création du groupe.<br/> Chaque groupe a un SID unique que le domaine du serveur Windows NT/Windows 2000 émet et qui est stocké dans l’attribut <strong>objectSID</strong> de l’objet de groupe dans l’annuaire. Chaque fois qu’un utilisateur ouvre une session, le système récupère le SID pour les groupes dont l’utilisateur est membre et le place dans le jeton d’accès de l’utilisateur. Le système utilise les SID dans le jeton d’accès de l’utilisateur pour identifier l’utilisateur et ses appartenances à des groupes dans toutes les interactions suivantes avec la sécurité Windows NT/Windows 2000.<br/> Lorsqu’un SID a été utilisé en tant qu’identificateur unique pour un utilisateur ou un groupe, il ne peut jamais être utilisé pour identifier un autre utilisateur ou groupe.<br/></td>
</tr>
<tr class="odd">
<td><strong>sAMAccountName</strong></td>
<td>L’attribut <strong>sAMAccountName</strong> est un attribut à valeur unique qui est le nom d’ouverture de session utilisé pour prendre en charge les clients et les serveurs d’une version antérieure (Windows 95, Windows 98 et LAN Manager). Le <strong>sAMAccountName</strong> doit comporter moins de 20 caractères pour prendre en charge les clients et les serveurs d’une version précédente.<br/> <strong>SAMAccountName</strong> doit être unique parmi tous les objets principaux de sécurité d’un domaine.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="group-types"></a>Types de groupes

Il existe deux types de groupes définis par Active Directory Domain Services, les groupes de *sécurité* et les *groupes de distribution*.

Un groupe de sécurité fournit un regroupement logique d’objets et le groupe lui-même peut être utilisé comme principal de sécurité dans une liste de Access Control (ACL). Lorsqu’un groupe de sécurité est autorisé à accéder à un objet, tous les membres du groupe de sécurité reçoivent automatiquement le même accès à l’objet. Les groupes de sécurité avec une étendue universelle peuvent également être utilisés comme une entité de messagerie. L’envoi d’un message électronique à un groupe de sécurité universel envoie le message à tous les membres du groupe.

Un groupe de distribution fournit également un regroupement logique d’objets, mais ne peut pas fournir de privilèges d’accès. Les groupes de distribution ne sont pas activés pour la sécurité et ne peuvent pas être utilisés comme principal de sécurité dans une liste de contrôle d’accès. Les groupes de distribution sont utilisés uniquement à des fins de regroupement. Par exemple, les listes de distribution peuvent être utilisées avec des applications de messagerie, telles qu’Exchange, pour envoyer des messages électroniques à un regroupement d’utilisateurs.

Pour plus d’informations sur les types de groupes dans Active Directory Domain Services, consultez la rubrique [types de groupes](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) sur [Microsoft TechNet](https://technet.microsoft.com/default.aspx).

## <a name="group-scope"></a>Étendue du groupe

Il existe trois étendues de groupe définies par Active Directory Domain Services, *Universal*, *Global* et *Domain local*. L’étendue du groupe définit les types d’objets qui peuvent appartenir au groupe, les types de groupes dont le groupe peut être membre et l’étendue des objets auxquels les groupes de sécurité peuvent accéder. Lorsque le niveau fonctionnel du domaine est défini sur Windows 2000 mode mixte, les groupes de sécurité avec une étendue universelle ne peuvent pas être créés.

Le tableau suivant répertorie les trois étendues de groupe et plus d’informations sur chaque étendue pour un groupe de sécurité.

| Étendue                   | Membres possibles                                                                                                                                                                                                                                      | Conversion d’étendue                                                                                                                                                 | Peut accorder des autorisations                                                       | Membre possible de                                                                                                                                                                                                  |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Universal<br/>    | Comptes issus de n’importe quel domaine de la même forêt.<br/> Groupes globaux de n’importe quel domaine de la même forêt.<br/> D’autres groupes universels de n’importe quel domaine de la même forêt.<br/>                                                            | Peut être converti en étendue de domaine local.<br/> Peut être convertie en portée globale tant que le groupe ne contient pas d’autres groupes universels.<br/> | Sur n’importe quel domaine de la même forêt ou des forêts de confiance.<br/>            | Autres groupes universels de la même forêt.<br/> Groupes locaux de domaine dans la même forêt ou dans les forêts d’approbation.<br/> Des groupes locaux sur des ordinateurs de la même forêt ou des forêts de confiance.<br/>            |
| Global<br/>       | Comptes du même domaine.<br/> Autres groupes globaux du même domaine.<br/>                                                                                                                                                        | Peut être converti en étendue universelle tant que le groupe n’est pas membre d’un autre groupe global.<br/>                                                   | Sur n’importe quel domaine de la même forêt ou des domaines ou forêts de confiance.<br/> | Groupes universels de n’importe quel domaine de la même forêt.<br/> Autres groupes globaux du même domaine.<br/> Groupes locaux de domaine de n’importe quel domaine de la même forêt ou de n’importe quel domaine d’approbation.<br/> |
| Domaine local<br/> | Comptes d’un domaine ou d’un domaine approuvé.<br/> Groupes globaux d’un domaine ou d’un domaine approuvé.<br/> Groupes universels de n’importe quel domaine de la même forêt.<br/> Autres groupes locaux de domaine du même domaine.<br/> | Peut être converti en étendue universelle tant que le groupe ne contient pas d’autres groupes locaux de domaine.<br/>                                              | Dans le même domaine.<br/>                                          | Autres groupes locaux de domaine du même domaine.<br/> Groupes locaux sur les ordinateurs du même domaine, à l’exception des groupes prédéfinis qui ont des SID bien connus.<br/>                                             |



 

 

