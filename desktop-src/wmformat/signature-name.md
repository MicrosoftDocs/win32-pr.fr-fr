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
ms.openlocfilehash: af378671a570dd9ffc58021081b3925d3dca21af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678522"
---
# <a name="signature_name"></a>Nom de la signature \_

L' **attribut \_ nom** de la signature contient le nom du certificat utilisé pour signer le fichier. Cet attribut est valide uniquement si l’attribut [**is \_ Trusted**](is-trusted.md) a la valeur true.

## <a name="global-constant"></a>Constante globale

\_nom wszWMSignature \_ g

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




