---
description: Cette vue d’ensemble introduit plusieurs méthodes XAudio2 que vous pouvez appeler dans le cadre d’un ensemble d’opérations.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Ensembles d’opérations XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210801"
---
# <a name="xaudio2-operation-sets"></a>Ensembles d’opérations XAudio2

Cette vue d’ensemble introduit plusieurs méthodes XAudio2 que vous pouvez appeler dans le cadre d’un ensemble d’opérations.

Plusieurs méthodes XAudio2 prennent l’argument *OperationSet* , ce qui leur permet d’être appelés dans le cadre d’un groupe différé. À un moment donné, vous pouvez appliquer un ensemble complet de modifications simultanément en appelant la fonction [**IXAudio2 :: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) avec l’identificateur *OperationSet* pour ce groupe. L’identificateur est un nombre arbitraire. Par conséquent, il permet à des parties distinctes du code client d’appliquer des modifications atomiques distinctes au graphique sans aucun conflit. La pratique recommandée consiste à ce que le client incrémente un compteur global chaque fois qu’il doit générer un nouvel identificateur *OperationSet* unique. Un ensemble de modifications apportées au graphique, appliqué atomiquement, est garanti comme étant exact. Par exemple, les voix commencent à se synchroniser.

Si vous affectez à *OperationSet* la valeur XAUDIO2 \_ Commit \_ Now, la modification s’applique immédiatement. Elle prend effet lors de la première passe de traitement audio après l’appel de la méthode. Si vous appelez [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) avec XAUDIO2 \_ Commit \_ All, les modifications apportées à tous les ensembles d’opérations en attente sont effectuées, quel que soit leur identificateur *OperationSet* .

Certaines méthodes prennent effet immédiatement quand elles sont appelées à partir d’un rappel XAudio2 avec un *OperationSet* de XAudio2 \_ valider \_ maintenant. Toutes les autres méthodes qui acceptent un argument *OperationSet* prennent effet uniquement lors du prochain passage de traitement après l’appel de la méthode (si elle est appelée avec XAUDIO2 \_ Commit \_ Now) ou après l’appel de [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) avec le même *OperationSet*. Pour cette raison, certains appels de méthode peuvent ne pas se produire toujours dans le même ordre que celui dans lequel ils ont été appelés.

Toutes les opérations en attente sont validées atomiquement lors de l’appel de [**IXAudio2 :: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) . Toutes les méthodes qui sont appelées pendant que le moteur est arrêté prennent effet immédiatement, quelle que soit la valeur *OperationSet* fournie. Lorsque vous redémarrez le moteur, XAudio2 revient en mode asynchrone.

Les scénarios les plus simples dans lesquels les ensembles d’opérations sont utiles incluent les exemples suivants.

-   Démarrage simultané de plusieurs voix.
-   Envoi simultané d’une mémoire tampon à une voix, définition des paramètres vocaux et démarrage de la voix.
-   En effectuant une modification à grande échelle du graphique, par exemple en connectant toutes les voix source à une nouvelle voix de mixage.

Consultez [Comment : regrouper des méthodes audio comme une opération définie](how-to--group-audio-methods-as-an-operation-set.md) pour obtenir un exemple d’utilisation d’un jeu d’opérations.

## <a name="operation-set-methods"></a>Méthodes de définition d’opérations

Vous pouvez appeler les méthodes suivantes dans le cadre d’un ensemble d’opérations.

-   [**IXAudio2SourceVoice :: ExitLoop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [**IXAudio2SourceVoice :: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [**IXAudio2Voice ::D isableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [**IXAudio2SourceVoice :: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [**IXAudio2SourceVoice :: Stop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

Comme décrit précédemment, le code client doit finalement appeler la fonction [**IXAudio2 :: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) pour exécuter les modifications différées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ensembles d’opérations](operation-sets.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : regrouper des méthodes audio comme un ensemble d’opérations](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
