---
description: Cette rubrique montre comment vous pouvez regrouper les méthodes XAudio2 afin qu’elles prennent effet en même temps.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 'Procédure : regrouper des méthodes audio comme un ensemble d’opérations'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5146c650ae6f89331c40f3e0db896f49484a6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866485"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="f69b7-103">Procédure : regrouper des méthodes audio comme un ensemble d’opérations</span><span class="sxs-lookup"><span data-stu-id="f69b7-103">How to: Group Audio Methods as an Operation Set</span></span>

<span data-ttu-id="f69b7-104">Cette rubrique montre comment vous pouvez regrouper les méthodes XAudio2 afin qu’elles prennent effet en même temps.</span><span class="sxs-lookup"><span data-stu-id="f69b7-104">This topic shows you how you can group together XAudio2 methods so they take effect at the same time.</span></span>

## <a name="to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="f69b7-105">Pour regrouper des méthodes audio comme un ensemble d’opérations</span><span class="sxs-lookup"><span data-stu-id="f69b7-105">To group audio methods as an operation set</span></span>

1.  <span data-ttu-id="f69b7-106">Déclarez un compteur d’ensemble d’opérations global.</span><span class="sxs-lookup"><span data-stu-id="f69b7-106">Declare a global operation set counter.</span></span>

    <span data-ttu-id="f69b7-107">Le compteur de l' [ensemble d’opérations](operation-sets.md) garantit que chaque ensemble d’opérations est unique.</span><span class="sxs-lookup"><span data-stu-id="f69b7-107">The [operation set](operation-sets.md) counter ensures that each operation set is unique.</span></span>

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  <span data-ttu-id="f69b7-108">Incrémentez le compteur global.</span><span class="sxs-lookup"><span data-stu-id="f69b7-108">Increment the global counter.</span></span>

    <span data-ttu-id="f69b7-109">Chaque fois que vous soumettez un nouveau [jeu d’opérations](operation-sets.md), le compteur global doit être incrémenté pour s’assurer que chaque ensemble est unique.</span><span class="sxs-lookup"><span data-stu-id="f69b7-109">Each time you submit a new [operation set](operation-sets.md), the global counter should increment to ensure each set is unique.</span></span>

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  <span data-ttu-id="f69b7-110">Regroupez les appels de méthode en définissant leurs paramètres d' [ensemble d’opérations](operation-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="f69b7-110">Group the method calls by setting their [operation set](operation-sets.md) parameters.</span></span>

4.  <span data-ttu-id="f69b7-111">Définissez les paramètres de l' [ensemble d’opérations](operation-sets.md) sur la valeur actuelle du compteur global.</span><span class="sxs-lookup"><span data-stu-id="f69b7-111">Set the [operation set](operation-sets.md) parameters to the current value of the global counter.</span></span>

    <span data-ttu-id="f69b7-112">Dans ce cas, quatre appels à [**IXAudio2SourceVoice :: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) sont regroupés comme un seul [ensemble d’opérations](operation-sets.md).</span><span class="sxs-lookup"><span data-stu-id="f69b7-112">In this case, four calls to [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) are grouped as one [operation set](operation-sets.md).</span></span> <span data-ttu-id="f69b7-113">En regroupant les appels, les quatre sons commencent exactement au même moment.</span><span class="sxs-lookup"><span data-stu-id="f69b7-113">Grouping the calls causes all four of the sounds to start at exactly the same time.</span></span>

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  <span data-ttu-id="f69b7-114">Démarrez le [jeu d’opérations](operation-sets.md).</span><span class="sxs-lookup"><span data-stu-id="f69b7-114">Start the [operation set](operation-sets.md).</span></span>

    <span data-ttu-id="f69b7-115">Après avoir appelé toutes les méthodes dans le jeu, démarrez le jeu en appelant [**IXAudio2 :: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) avec la valeur actuelle du compteur global.</span><span class="sxs-lookup"><span data-stu-id="f69b7-115">After you call all the methods in the set, start the set by calling [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the current value of the global counter.</span></span>

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="f69b7-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f69b7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f69b7-117">Ensembles d’opérations</span><span class="sxs-lookup"><span data-stu-id="f69b7-117">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="f69b7-118">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="f69b7-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="f69b7-119">Ensembles d’opérations XAudio2</span><span class="sxs-lookup"><span data-stu-id="f69b7-119">XAudio2 Operation Sets</span></span>](xaudio2-operation-sets.md)
</dt> </dl>

 

 
