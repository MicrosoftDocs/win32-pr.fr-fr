---
description: La méthode GetVendorString récupère le nom du fournisseur. Pour les objets de moteur de rendu fournis par DirectShow, la chaîne du fournisseur est &\# 0034 ; Microsoft Corporation&\# 0034 ;.
ms.assetid: d0a4c525-67dc-419a-b4d6-8cd51888fd8a
title: 'IRenderEngine :: GetVendorString, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetVendorString
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abf339b73fa058c6554965c16428774ad1fdd32c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540585"
---
# <a name="irenderenginegetvendorstring-method"></a>IRenderEngine :: GetVendorString, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetVendorString` méthode récupère le nom du fournisseur. Pour les objets de moteur de rendu fournis par DirectShow, la chaîne du fournisseur est « Microsoft Corporation ».

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVendorString(
  [out, retval] BSTR *pVendorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVendorID* \[ out, retval\]
</dt> <dd>

Reçoit un **BSTR** contenant la chaîne du fournisseur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

La méthode alloue de la mémoire pour la chaîne. L’application doit appeler **SysFreeString** pour libérer la mémoire.

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

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




