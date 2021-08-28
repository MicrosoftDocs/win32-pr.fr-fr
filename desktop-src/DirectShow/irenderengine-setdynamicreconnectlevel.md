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
ms.openlocfilehash: b43967753dd03d213a322ce569d113346542a57b5f37fd69fc28937198109049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083679"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a>IRenderEngine :: SetDynamicReconnectLevel, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

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
| <dl> <dt>**\_OK**</dt> </dl>      | Réussite.<br/>         |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl> | Non implémenté.<br/> |



 

## <a name="remarks"></a>Remarques

Par défaut, le moteur de rendu de base charge chaque source avant d’effectuer le rendu d’un projet. Cela peut se traduire par un temps de démarrage long. Avec la reconnexion dynamique, les sources sont chargées uniquement lorsque cela est nécessaire. Cela peut raccourcir le temps de démarrage, mais risque d’interférer avec la lecture en douceur. En règle générale, plus le nombre d’éléments sources utilisés par un projet est grand, plus vous pouvez tirer parti de la reconnexion dynamique.

Le moteur de rendu intelligent n’implémente pas cette méthode.

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

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




