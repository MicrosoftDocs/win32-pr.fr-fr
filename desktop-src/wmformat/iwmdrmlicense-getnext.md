---
title: IWMDRMLicense GetNext, méthode (wmdrmsdk. h)
description: La méthode GetNext charge les informations relatives à l’élément suivant de la liste.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- Méthode GetNext Windows Media format
- Méthode GetNext Windows Media format, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, GetNext, méthode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528681"
---
# <a name="iwmdrmlicensegetnext-method"></a>IWMDRMLicense :: GetNext, méthode

La méthode **GetNext** charge les informations relatives à l’élément suivant de la liste.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNext();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                | Description                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt> </dl> | Une liste de révocation de contenu mise à jour est nécessaire.<br/> |
| <dl> <dt>**ERREUR \_ aucun \_ autre \_ élément**</dt> </dl>      | Il n’y a plus d’élément dans la liste.<br/>          |
| <dl> <dt>**\_OK**</dt> </dl>                       | S_OK<br/>                         |



 

## <a name="remarks"></a>Notes

Les méthodes de l’interface [**IWMDRMLicense**](iwmdrmlicense.md) fournissent des données sur une licence unique à la fois. L’objet sous-jacent contient une liste d’une ou de plusieurs licences. Lorsque vous appelez cette méthode, l’interface déplace ses références internes à la licence suivante dans la liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





