---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f84d56ba74325b6c65fb5c06ba2db9228c78d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318489"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt

L’élément **MBNProfileExt** est une extension de l’élément MBNProfile précédent. Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.

Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement. Utilisez l’élément enfant [**ProfileConditionedOn**](element-profileconditionedon.md) de **MBNProfileExt** pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

**<MBNProfileExt>**

## <a name="syntax"></a>Syntaxe

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a>Clé

`?`   facultatif (zéro ou un)

`*`   facultatif (zéro, un ou plusieurs)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs

Aucun

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément enfant</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-adminenable.md">AdminEnable</a></td>
<td><p>Spécifie si le profil est activé de manière administrative. Il s’agit d’un nouvel élément pour v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-adminroamcontrol.md">AdminRoamControl</a></td>
<td><p>Spécifie si le profil est contrôlé par un itinérance administrative. Cet élément est une nouveauté pour v4. La valeur de cet élément est une valeur <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> . Il s’agit d’un élément facultatif ; Si aucune valeur n’est spécifiée, <strong>AllRoamAllowed</strong> est la valeur par défaut.</p></td>
</tr>
<tr class="odd">
<td><a href="element-apnid.md">ApnID</a></td>
<td><p>ID APN associé à ce profil. Cet élément est une nouveauté de V4 et il est facultatif.</p></td>
</tr>
<tr class="even">
<td><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></td>
<td><p>Spécifie si l’appareil haut débit mobile se connecte automatiquement à un réseau.</p>
<p>Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-connectionmode.md">ConnectionMode</a></td>
<td><p>Spécifie le paramètre de connexion automatique à utiliser pour un appareil haut débit mobile.</p>
<p>Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-context.md">Contexte</a></td>
<td><p>Spécifie les paramètres requis pour établir une connexion de données.</p></td>
</tr>
<tr class="odd">
<td><a href="element-dataroamingpartners.md">DataRoamingPartners</a></td>
<td><p>Spécifie une liste de fournisseurs de réseau préférés lors de l’itinérance.</p>
<p>Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-description.md">Description</a></td>
<td><p>Description du profil.</p></td>
</tr>
<tr class="odd">
<td><a href="element-homeprovidername.md">HomeProviderName</a></td>
<td><p>Nom du fournisseur d’hébergement pour la carte SIM/le périphérique donné. Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-iconfilepath.md">ICONFilePath</a></td>
<td><p>Chemin d’accès au fichier d’icône pour la connexion. L’interface utilisateur de la connexion au système d’exploitation affiche l’icône lorsqu’une connexion est établie à l’aide de ce profil.</p>
<p>Pour plus d’informations sur l’utilisation de cet élément, consultez la documentation v1 pour <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</p></td>
</tr>
<tr class="odd">
<td><a href="element-isdefault.md">IsDefault</a></td>
<td><p>Spécifie si ce profil est le profil par défaut.</p>
<p>Pour plus d’informations sur cet élément, consultez la documentation v1 pour <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</p></td>
</tr>
<tr class="even">
<td><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></td>
<td><p>Spécifie que ce profil est exclusif à d’autres profils du ou des mêmes jeux de profils. Cet élément est une nouveauté pour v4.</p></td>
</tr>
<tr class="odd">
<td><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></td>
<td><p>Spécifie que ce profil est un profil de contexte PDP supplémentaire à long terme. Si la valeur de cet élément est <strong>true</strong>, <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> doit également être défini sur <strong>true</strong>. Il s’agit d’un nouvel élément pour v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></td>
<td><p>Spécifie que ce profil ne doit être utilisé que pour l’approvisionnement. Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol). Cet élément est une nouveauté pour v4.</p>
<p>Si <strong>IsProvisioningProfile</strong> a la valeur true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> doit avoir la valeur false et <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> doit être manuel.</p></td>
</tr>
<tr class="odd">
<td><a href="element-mmsconfiguration.md">MmsConfiguration</a></td>
<td><p>Informations de configuration pour le service de messagerie multimédia (MMS).</p>
<p>En plus de définir les éléments de configuration dans cet élément, un profil MMS doit avoir les paramètres suivants.</p>
<ul>
<li>Son élément <a href="element-name.md"><strong>Name</strong></a> doit contenir un nom unique à l’ensemble du système.</li>
<li>Son <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> doit avoir la valeur <strong>UserProvisioned</strong>.</li>
<li>Son <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> doit contenir le ICCID de la carte SIM auquel ce profil est destiné.</li>
<li>Son <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> doit être défini sur <strong>Manuel</strong>.</li>
<li>Son <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> doit contenir le GUID du groupe d’objet MMS.</li>
<li>Son <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> doit avoir la valeur <strong>true</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="element-name.md">Nom</a></td>
<td><p>Nom du profil. Pour plus d’informations, consultez la documentation de l’élément de <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nom</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-profileconditionedon.md">ProfileConditionedOn</a></td>
<td><p>Spécifie les conditions qui doivent être satisfaites pour qu’un profil soit applicable.</p>
<p>Cet élément est une nouveauté pour v4. Elle vous permet de spécifier plusieurs profils qui s’appliquent dans différentes conditions, et pour que le profil approprié soit utilisé automatiquement lorsqu’il est applicable. Cet élément est facultatif. Si vous ne le spécifiez pas, le profil est toujours applicable en ce qui concerne les conditions indiquées.</p></td>
</tr>
<tr class="even">
<td><a href="element-profilecreationtype.md">ProfileCreationType (dans MBNProfileExt)</a></td>
<td><p>Spécifie le créateur du profil.</p>
<p>Pour plus d’informations sur cet élément, consultez la documentation de l’élément <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-purposegroups.md">PurposeGroups</a></td>
<td><p>Liste facultative de groupes de profils, où chaque groupe comprend des profils utilisés dans un but commun.</p>
<p>Cet élément est une nouveauté pour v4 du schéma.</p>
<p>Un profil peut être listé dans plusieurs groupes.</p></td>
</tr>
<tr class="even">
<td><a href="element-simiccid.md">SimIccID</a></td>
<td><p>Numéro de identifcation SIM pour les appareils GSM. Pour plus d’informations, consultez la documentation de l’élément <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-subscriberid.md">Abonné</a></td>
<td><p>Identifie l’identificateur unique du profil.</p>
<p>Pour un réseau GSM, il doit contenir le IMSI (identité de l’abonné mobile international) de la carte SIM et des appareils CDMA. il doit contenir la valeur minimale (numéro d’identification mobile) de l’appareil.</p>
<p>Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>abonné</strong></a> v1.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents

Cet élément (document) le plus à l’extérieur ne peut pas être contenu dans d’autres éléments.

## <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Espace de noms</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
