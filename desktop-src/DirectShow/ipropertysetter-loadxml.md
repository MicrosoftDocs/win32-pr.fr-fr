---
description: La méthode LoadXML charge des données de propriété exprimées en Extensible Markup Language (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'IPropertySetter :: LoadXML, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1779c6bcd37baad4bd423d0a46abd3741dd3a7939c1615a5871e6746729558c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952568"
---
# <a name="ipropertysetterloadxml-method"></a>IPropertySetter :: LoadXML, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `LoadXML` méthode charge des données de propriété exprimées en Extensible Markup Language (XML).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pXML* \[ dans\]
</dt> <dd>

Pointeur vers l’interface **IUnknown** d’un élément XML créé par l’analyseur XML Microsoft.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                                  | Description                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                      | Aucune donnée de propriété.<br/>    |
| <dl> <dt>**\_OK**</dt> </dl>                         | Réussite.<br/>             |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>                | Mémoire insuffisante.<br/> |
| <dl> <dt>**VFW \_ E \_ \_ format de fichier non valide \_**</dt> </dl> | Format non valide.<br/>      |



 

## <a name="remarks"></a>Remarques

En règle générale, les applications n’ont pas besoin d’utiliser cette méthode. DES l’utilise en interne pour charger des propriétés à partir de fichiers XTL.

Pour utiliser cette méthode, créez un objet **IXMLDocument** et utilisez-le pour analyser un fichier XML. Utilisez ensuite l’objet **IXMLDocument** pour récupérer des objets **IXMLElement** . Si l’objet possède des propriétés, vous pouvez passer le pointeur **IXMLElement** à la méthode **LoadXml** . La méthode charge les propriétés dans l’accesseur Set de propriété.

> [!Note]  
> les interfaces **IXMLDocument** et **IXMLElement** sont implémentées dans la version 1,0 de Microsoft XML Core Services® (MSXML), mais elles ne sont pas implémentées dans les versions plus récentes de MSXML.

 

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




