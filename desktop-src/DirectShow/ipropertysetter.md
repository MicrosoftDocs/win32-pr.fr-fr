---
description: 'l’interface IPropertySetter définit les propriétés d’un effet ou d’une transition dans DirectShow Services d’édition (DES). Pour utiliser cette interface, créez une instance d’un objet d’accesseur Set de propriété (CLSID \_ PropertySetter) et associez-la à un effet ou une transition en appelant la méthode IAMTimelineObj :: SetPropertySetter. Pour plus d’informations, consultez Utilisation des effets et des transitions. en général, une application doit appeler uniquement la méthode IPropertySetter :: ClearProps pour effacer les propriétés existantes, et la méthode IPropertySetter :: AddProp pour ajouter de nouvelles propriétés. Les autres méthodes sur cette interface sont appelées par d’autres composants DES.'
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Interface IPropertySetter (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c6dc32c25c85893eeb2e9872bcf67be974489ec82fdd4d09c19a2341f6867ade
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831029"
---
# <a name="ipropertysetter-interface"></a>Interface IPropertySetter

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IPropertySetter` interface définit des propriétés sur un effet ou une transition dans les [Services d’édition de DirectShow](directshow-editing-services.md) .

Pour utiliser cette interface, créez une instance d’un objet d’accesseur Set de propriété (CLSID \_ PropertySetter) et associez-la à un effet ou une transition en appelant la méthode [**IAMTimelineObj :: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) . Pour plus d’informations, consultez [utilisation des effets et des transitions](working-with-effects-and-transitions.md).

En règle générale, une application doit appeler uniquement la méthode [**IPropertySetter :: ClearProps**](ipropertysetter-clearprops.md) pour effacer les propriétés existantes, et la méthode [**IPropertySetter :: AddProp**](ipropertysetter-addprop.md) pour ajouter de nouvelles propriétés. Les autres méthodes sur cette interface sont appelées par d’autres composants DES.

## <a name="members"></a>Membres

L’interface **IPropertySetter** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IPropertySetter** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IPropertySetter** possède ces méthodes.



| Méthode                                               | Description                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddProp**](ipropertysetter-addprop.md)           | Ajoute une propriété à la méthode setter de propriété, avec un tableau de paires heure-valeur qui définissent la valeur de la propriété sur une plage de temps.<br/> |
| [**ClearProps**](ipropertysetter-clearprops.md)     | Efface toutes les données de propriété de l’accesseur Set de propriété.<br/>                                                                                 |
| [**CloneProps**](ipropertysetter-cloneprops.md)     | Clone un ensemble de propriétés à partir de cet accesseur Set de propriété et les ajoute à un nouvel accesseur Set de propriété.<br/>                                       |
| [**FreeProps**](ipropertysetter-freeprops.md)       | Libère les ressources allouées par la méthode [**IPropertySetter :: GetProps**](ipropertysetter-getprops.md) .<br/>                             |
| [**GetProps**](ipropertysetter-getprops.md)         | Récupère les propriétés définies sur cet objet, avec leurs valeurs correspondantes.<br/>                                                      |
| [**LoadFromBlob**](ipropertysetter-loadfromblob.md) | Charge des données de propriété à partir d’un format de persistance.<br/>                                                                                     |
| [**LoadXML**](ipropertysetter-loadxml.md)           | Charge des données de propriété exprimées en Extensible Markup Language (XML).<br/>                                                                 |
| [**PrintXML**](ipropertysetter-printxml.md)         | Convertit des données de propriété en une chaîne XML.<br/>                                                                                         |
| [**SaveToBlob**](ipropertysetter-savetoblob.md)     | Enregistre les données de propriété dans un format de persistance.<br/>                                                                                   |
| [**SetProps**](ipropertysetter-setprops.md)         | Définit les propriétés de l’objet cible à l’état approprié pour l’heure spécifiée.<br/>                                          |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
