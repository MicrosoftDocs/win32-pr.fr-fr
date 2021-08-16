---
description: La \_ méthode put Size définit la taille de sortie et le mode Stretch.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: IResize ::p ut_Size, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d2da95cca7bf19182dd4c0f5f385715256ae9c5253c356094110c028fb1b016d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818129"
---
# <a name="iresizeput_size-method"></a>IResize : méthode de taille de :p ut \_

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `put_Size` méthode définit la taille de sortie et le mode Stretch.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Hauteur* \[ dans\]
</dt> <dd>

Hauteur vidéo, en pixels.

</dd> <dt>

*Largeur* \[ dans\]
</dt> <dd>

Largeur de la vidéo, en pixels.

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Mode Stretch. Pour connaître les valeurs possibles, consultez [**indicateurs de redimensionnement**](resize-flags.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

DES peuvent appeler cette méthode avant ou après l’appel à **put \_ MediaType**. Si la méthode DES appelle cette méthode avant d’appeler **put \_ MediaType**, le filtre doit sélectionner une valeur par défaut pour la profondeur de bits et utiliser les valeurs size pour construire un type de média de sortie. Si la méthode DES appelle cette méthode après avoir appelé **put \_ MediaType**, le filtre doit modifier son type de sortie actuel avec les nouvelles tailles.

DES peuvent également appeler cette méthode une fois que la broche de sortie est connectée. Dans ce cas, modifiez le type de sortie et reconnectez la broche de sortie avec le nouveau type. Pour plus d’informations, consultez [reconnexion des codes confidentiels](reconnecting-pins.md) .

Le paramètre *Flags* spécifie la manière dont le filtre doit effectuer l’opération de redimensionnement.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9,0 ou version ultérieure<br/>                                                         |
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> <dt>

[**Interface IResize**](iresize.md)
</dt> </dl>

 

 




