---
title: Signature_Name
description: L' \_ attribut nom de la signature contient le nom du certificat utilisé pour signer le fichier. Cet attribut est valide uniquement si l' \_ attribut is Trusted a la valeur true.
ms.assetid: 3f3ab10c-731b-4075-8f73-3c2e62e010b9
keywords:
- Format Windows Media Signature_Name
topic_type:
- apiref
api_name:
- Signature_Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bff0516353468733ef5c834d51dddc7bbc85e322d98b82929e092913bc375a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845850"
---
# <a name="signature_name"></a>Nom de la signature \_

L' **attribut \_ nom** de la signature contient le nom du certificat utilisé pour signer le fichier. Cet attribut est valide uniquement si l’attribut [**is \_ Trusted**](is-trusted.md) a la valeur true.

## <a name="global-constant"></a>Constante globale

\_nom wszWMSignature \_ g

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) de Format multimédia Windows.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




