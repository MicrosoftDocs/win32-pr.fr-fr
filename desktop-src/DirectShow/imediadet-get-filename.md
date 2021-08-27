---
description: La méthode obtenir un nom \_ de fichier récupère le nom du fichier source actuellement utilisé par le détecteur de média.
ms.assetid: 68f0f1ea-74a2-4b65-9f1d-8699326d9d04
title: 'IMediaDet :: get_Filename, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a705291155adc848b107c0950e77a63ed181b052dc71cd72d128ebca1be980b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952588"
---
# <a name="imediadetget_filename-method"></a>IMediaDet :: obten, \_ méthode de nom de fichier

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_Filename` méthode récupère le nom du fichier source actuellement utilisé par le détecteur de média.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Filename(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit le nom de fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

La méthode alloue de la mémoire pour la chaîne. L’application doit appeler **SysFreeString** pour libérer la mémoire.

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

[**Interface IMediaDet**](imediadet.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




