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
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539577"
---
# <a name="ipropertysetterloadxml-method"></a>IPropertySetter :: LoadXML, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

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
| <dl> <dt>**\_OK**</dt> </dl>                         | Opération réussie.<br/>             |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>                | Mémoire insuffisante.<br/> |
| <dl> <dt>**VFW \_ E \_ \_ format de fichier non valide \_**</dt> </dl> | Format non valide.<br/>      |



 

## <a name="remarks"></a>Notes

En règle générale, les applications n’ont pas besoin d’utiliser cette méthode. DES l’utilise en interne pour charger des propriétés à partir de fichiers XTL.

Pour utiliser cette méthode, créez un objet **IXMLDocument** et utilisez-le pour analyser un fichier XML. Utilisez ensuite l’objet **IXMLDocument** pour récupérer des objets **IXMLElement** . Si l’objet possède des propriétés, vous pouvez passer le pointeur **IXMLElement** à la méthode **LoadXml** . La méthode charge les propriétés dans l’accesseur Set de propriété.

> [!Note]  
> Les interfaces **IXMLDocument** et **IXMLElement** sont implémentées dans Microsoft XML Core Services (MSXML) version 1,0, mais elles ne sont pas implémentées dans les versions plus récentes de MSXML.

 

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

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

 

 




