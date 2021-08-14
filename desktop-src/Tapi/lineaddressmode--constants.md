---
description: Les \_ constantes d’indicateur de bit LINEADDRESSMODE décrivent les différentes façons d’identifier une adresse sur un appareil de ligne.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: Constantes LINEADDRESSMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4863b79c4527395f6ecb2d28c4d9ef718ff5a7fd99681185ba892bac2b4639ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761861"
---
# <a name="lineaddressmode_-constants"></a>\_Constantes LINEADDRESSMODE

Les constantes d’indicateur de bit **LINEADDRESSMODE \_** décrivent les différentes façons d’identifier une adresse sur un appareil de ligne.

<dl> <dt>

<span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ ADDRESSID**
</dt> <dd> <dl> <dt>



L’adresse est spécifiée avec un petit entier compris entre 0 et *dwNumAddresses* moins un, où *dwNumAddresses* est la valeur dans les capacités de l’appareil de la ligne.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**
</dt> <dd> <dl> <dt>



L’adresse est spécifiée par son numéro de téléphone.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil. Les 16 bits de poids faible sont réservés.

Cette constante est utilisée pour sélectionner une adresse sur une ligne sur laquelle un appel doit être généré. Le modèle habituel sélectionne l’adresse à l’aide de son identificateur d’adresse. Les identificateurs d’adresse sont le mécanisme utilisé pour identifier les adresses dans l’interface TAPI. Toutefois, dans certains environnements, lors de la création d’un appel, il est souvent plus pratique d’identifier l’adresse d’origine d’un appel par numéro de téléphone plutôt que par identificateur d’adresse. Par exemple, la modélisation possible d’un grand nombre de stations (tierces) sur le commutateur à l’aide d’un périphérique de ligne avec de nombreuses adresses. La ligne représente l’ensemble de toutes les stations, et chaque station est mappée à une adresse avec son propre numéro de téléphone principal et son identificateur d’adresse.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




