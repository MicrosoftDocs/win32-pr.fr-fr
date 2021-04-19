---
description: La méthode SetDynamicReconnectLevel définit le niveau de reconnexion dynamique lors du rendu.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'IRenderEngine :: SetDynamicReconnectLevel, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543864"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a>IRenderEngine :: SetDynamicReconnectLevel, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetDynamicReconnectLevel` méthode définit le niveau de reconnexion dynamique lors du rendu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Niveau* 
</dt> <dd>

Combinaison d' [**indicateurs de reconnexion dynamique**](dynamic-reconnection-flags.md), spécifiant le niveau de reconnexion dynamique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                               | Description                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Opération réussie.<br/>         |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl> | Non implémenté.<br/> |



 

## <a name="remarks"></a>Notes

Par défaut, le moteur de rendu de base charge chaque source avant d’effectuer le rendu d’un projet. Cela peut se traduire par un temps de démarrage long. Avec la reconnexion dynamique, les sources sont chargées uniquement lorsque cela est nécessaire. Cela peut raccourcir le temps de démarrage, mais risque d’interférer avec la lecture en douceur. En règle générale, plus le nombre d’éléments sources utilisés par un projet est grand, plus vous pouvez tirer parti de la reconnexion dynamique.

Le moteur de rendu intelligent n’implémente pas cette méthode.

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

 

 




