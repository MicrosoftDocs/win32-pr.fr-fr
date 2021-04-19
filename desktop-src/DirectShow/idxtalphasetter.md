---
description: L’interface IDxtAlphaSetter définit les propriétés sur l’effet d’accesseur Set alpha. Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de l’effet d’accesseur Set alpha.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Interface IDxtAlphaSetter (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530999"
---
# <a name="idxtalphasetter-interface"></a>Interface IDxtAlphaSetter

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IDxtAlphaSetter` interface définit les propriétés sur l’effet d' [accesseur Set alpha](alpha-setter-effect.md) .

Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de l’effet d’accesseur Set alpha. Les applications DES n’ont pas besoin d’utiliser cette interface. Pour définir les propriétés d’une transition dans DES, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Membres

L’interface **IDxtAlphaSetter** hérite de **IDXEffect**. **IDxtAlphaSetter** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDxtAlphaSetter** possède ces méthodes.



| Méthode                                                  | Description                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [**récupération \_ alpha**](idxtalphasetter-get-alpha.md)         | Récupère la valeur alpha de la totalité de l’image.<br/> |
| [**Obtient \_ AlphaRamp**](idxtalphasetter-get-alpharamp.md) | Récupère la propriété de rampe alpha.<br/>              |
| [**put \_ alpha**](idxtalphasetter-put-alpha.md)         | Spécifie la valeur alpha de la totalité de l’image.<br/> |
| [**put \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md) | Spécifie la propriété de rampe alpha.<br/>              |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 




