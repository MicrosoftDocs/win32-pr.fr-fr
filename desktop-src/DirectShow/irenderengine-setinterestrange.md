---
description: 'IRenderEngine :: SetInterestRange, méthode non prise en charge.'
ms.assetid: 1e4c3bd4-2540-428f-9ca6-dd4c65c53434
title: 'IRenderEngine :: SetInterestRange, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetInterestRange
api_type:
- COM
api_location: ''
ms.openlocfilehash: ec9790e65efa30b83cf324da4153f20c541733b9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084457"
---
# <a name="irenderenginesetinterestrange-method"></a>IRenderEngine :: SetInterestRange, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée dans les versions futures de Windows.\]

 

Non pris en charge.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Start* 
</dt> <dd>

Réservé.

</dd> <dt>

*Stop* 
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes 

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IRenderEngine**](irenderengine.md)
</dt> </dl>

 

 



