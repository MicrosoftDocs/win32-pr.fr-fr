---
description: La méthode SetBufferSamples spécifie s’il faut copier les exemples de données dans une mémoire tampon à mesure qu’elle passe par le filtre.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'ISampleGrabber :: SetBufferSamples, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c768a21d4e08e6900f3a46f3e398f5040aaf6b6b0bc45c9187ac07821500a372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817994"
---
# <a name="isamplegrabbersetbuffersamples-method"></a>ISampleGrabber :: SetBufferSamples, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La méthode **SetBufferSamples** spécifie s’il faut copier les exemples de données dans une mémoire tampon à mesure qu’elle passe par le filtre.

## <a name="syntax"></a>Syntaxe


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*BufferThem* 
</dt> <dd>

Valeur booléenne spécifiant si les exemples de données doivent être mis en mémoire tampon. Si la **valeur est true**, le filtre copie les exemples de données dans une mémoire tampon interne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Pour récupérer la mémoire tampon copiée, appelez [**ISampleGrabber :: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).

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

[Utilisation de l’exemple d’accrochage](using-the-sample-grabber.md)
</dt> <dt>

[**Interface ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




