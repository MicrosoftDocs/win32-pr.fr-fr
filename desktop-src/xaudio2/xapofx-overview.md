---
description: XAPOFX est une collection d’effets audio implémentant les interfaces XAPO à utiliser dans XAudio2. XAPOFX contient plusieurs effets et un mécanisme commun pour créer des instances d’effet.
ms.assetid: 762062de-4e19-5e42-8059-e2f8741bd362
title: Présentation de XAPOFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae339a022ae5e2e880dcd130dbe055d0fde9cd28a95ea52c1238e2ade080ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005719"
---
# <a name="xapofx-overview"></a>Présentation de XAPOFX

XAPOFX est une collection d’effets audio implémentant les interfaces [XAPO](xapo-overview.md) à utiliser dans XAudio2. XAPOFX contient plusieurs effets et un mécanisme commun pour créer des instances d’effet.

## <a name="included-effects"></a>Effets inclus

Le tableau suivant décrit les effets inclus dans XAPOFX. 

| Effet             | Description                                                                                                                                                                                           | Structure de paramètre                                                     | Constantes de paramètre                                              | Configuration requise                                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| FXECHO             | Effet d’écho.                                                                                                                                                                                       | [**\_paramètres FXECHO**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                         | [**Constantes FXECHO**](fxecho-constants.md)                     | Prend uniquement en charge les formats audio FLOAT32.                                                                                      |
| FXEQ               | Égaliseur à quatre bandes.                                                                                                                                                                                | [**\_paramètres FXEQ**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                             | [**Constantes FXEQ**](fxeq-constants.md)                         | Prend uniquement en charge les formats audio FLOAT32. Le taux d’échantillonnage doit être compris entre 22 000 Hz et 48 000 Hz.                             |
| FXMasteringLimiter | Limite de volume.                                                                                                                                                                                     | [**\_paramètres FXMASTERINGLIMITER**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters) | [**Constantes FXMASTERINGLIMIT**](fxmasteringlimit-constants.md) | Prend uniquement en charge les formats audio FLOAT32.                                                                                      |
| FXReverb           | Effet de réverbération simple.<br/> XAudio2 fournit également un effet d’implémentation de la réverbération numérique de Princeton qui peut être instanciée avec [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb).<br/> | [**\_paramètres FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                     | [**Constantes FXREVERB**](fxreverb-constants.md)                 | Prend uniquement en charge les formats audio FLOAT32. En outre, il prend uniquement en charge l’entrée mono vers une sortie mono et une entrée stéréo vers une sortie stéréo. |



 

## <a name="creating-an-instance-of-an-effect-included-in-xapofx"></a>Création d’une instance d’un effet inclus dans XAPOFX

XAPOFX fournit la fonction [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) en tant que mécanisme commun pour créer des instances d’effet. **CreateFX** prend le CLSID d’un effet et retourne un pointeur d’interface IUnknown vers une instance de l’effet.

## <a name="using-xapofx-in-xaudio2"></a>Utilisation de XAPOFX dans XAudio2

Les effets instanciés avec [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) sont utilisés dans XAudio2 en les joignant à des voix. Chaque voix XAudio2 a une chaîne d’effet contenant zéro ou plusieurs effets audio. Les données audio envoyées à une voix sont transmises à chaque effet de la chaîne avant d’être envoyées aux cibles de sortie de la voix. La voix prend la sortie de chaque effet et l’alimente dans l’effet suivant de la chaîne jusqu’à ce qu’aucun effet ne reste dans la chaîne. Pour attacher un effet XAPOFX à une voix XAudio2, remplissez une structure [**de \_ \_ chaîne d’effet XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) avec les informations de l’effet et transmettez-la à [**IXAudio2Voice :: SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain).

Pour plus d’informations sur les chaînes d’effets XAudio2, consultez [effets audio XAudio2](xaudio2-audio-effects.md).

Pour obtenir un exemple d’utilisation de XAPOFX dans XAudio2, consultez [How to : Use XAPOFX in XAudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="xaudio2-implicit-effects"></a>XAudio2 les effets implicites

En plus de la bibliothèque de XAPOs fournie par XAPOFX, XAudio2 a des effets audio de réverbération et de contrôle de volume intégrés. Vous pouvez créer ces effets intégrés avec [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) et [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter). Pour obtenir un exemple d’utilisation de l’un de ces effets intégrés, consultez [How to : Create a Effect Chain](how-to--create-an-effect-chain.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets audio](audio-effects.md)
</dt> </dl>

 

 
