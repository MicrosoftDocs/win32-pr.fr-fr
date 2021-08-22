---
description: Cette rubrique montre comment vous pouvez regrouper les méthodes XAudio2 afin qu’elles prennent effet en même temps.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 'Procédure : regrouper des méthodes audio comme un ensemble d’opérations'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f5c1d27e33db4c0f7910761a7be574b72e9ac7aaa91b14329fa003792860d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082923"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a>Procédure : regrouper des méthodes audio comme un ensemble d’opérations

Cette rubrique montre comment vous pouvez regrouper les méthodes XAudio2 afin qu’elles prennent effet en même temps.

## <a name="to-group-audio-methods-as-an-operation-set"></a>Pour regrouper des méthodes audio comme un ensemble d’opérations

1.  Déclarez un compteur d’ensemble d’opérations global.

    Le compteur de l' [ensemble d’opérations](operation-sets.md) garantit que chaque ensemble d’opérations est unique.

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  Incrémentez le compteur global.

    Chaque fois que vous soumettez un nouveau [jeu d’opérations](operation-sets.md), le compteur global doit être incrémenté pour s’assurer que chaque ensemble est unique.

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  Regroupez les appels de méthode en définissant leurs paramètres d' [ensemble d’opérations](operation-sets.md) .

4.  Définissez les paramètres de l' [ensemble d’opérations](operation-sets.md) sur la valeur actuelle du compteur global.

    Dans ce cas, quatre appels à [**IXAudio2SourceVoice :: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) sont regroupés comme un seul [ensemble d’opérations](operation-sets.md). En regroupant les appels, les quatre sons commencent exactement au même moment.

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  Démarrez le [jeu d’opérations](operation-sets.md).

    Après avoir appelé toutes les méthodes dans le jeu, démarrez le jeu en appelant [**IXAudio2 :: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) avec la valeur actuelle du compteur global.

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ensembles d’opérations](operation-sets.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Ensembles d’opérations XAudio2](xaudio2-operation-sets.md)
</dt> </dl>

 

 
