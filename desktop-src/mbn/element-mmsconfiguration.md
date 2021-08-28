---
description: MmsConfiguration
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsConfiguration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6612ce37bfa39b9498b6db4b9ce49cb06a6326
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982132"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration

Informations de configuration pour le service de messagerie multimédia (MMS).

En plus de définir les éléments de configuration dans cet élément, un profil MMS doit avoir les paramètres suivants.

-   Son élément [**Name**](element-name.md) doit contenir un nom unique à l’ensemble du système.
-   Son [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) doit avoir la valeur **UserProvisioned**.
-   Son [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) doit contenir le ICCID de la carte SIM auquel ce profil est destiné.
-   Son [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) doit être défini sur **Manuel**.
-   Son [**PurposeGroupGuid**](element-purposegroupguid.md) doit contenir le GUID du groupe d’objet MMS.
-   Son [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) doit avoir la valeur **true**.

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;MmsConfiguration&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
```

### <a name="key"></a>Clé :

`?`   facultatif (zéro ou un)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs

Aucun.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants


| Élément enfant | Description | 
|---------------|-------------|
| <a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a> | <p>Spécifie la taille maximale, en kilo-octets, des messages MMS. facultatif.</p> | 
| <a href="element-mmscport.md">MmscPort</a> | <p>Spécifie le numéro de port du serveur MMSC pour l’appareil. Spécifiez 0 pour indiquer qu’aucun port spécifique n’est spécifié. facultatif.</p> | 
| <a href="element-mmscurl.md">MmscUrl</a> | <p>Spécifie l’URL du serveur MMSC pour l’appareil. facultatif.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents


| Élément parent | Description | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent. Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</p><p>Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement. Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</p> | 


 

## <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p>Espace de noms</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
