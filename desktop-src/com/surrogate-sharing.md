---
title: Partage de substitution
description: Les serveurs DLL partagent un substitut s’ils ont des identités de sécurité correspondantes et partagent la même valeur AppID.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672482"
---
# <a name="surrogate-sharing"></a><span data-ttu-id="67e50-103">Partage de substitution</span><span class="sxs-lookup"><span data-stu-id="67e50-103">Surrogate Sharing</span></span>

<span data-ttu-id="67e50-104">Les serveurs DLL partagent un substitut s’ils ont des identités de sécurité correspondantes et partagent la même valeur AppID.</span><span class="sxs-lookup"><span data-stu-id="67e50-104">DLL servers will share a surrogate if they have matching security identities and share the same AppID value.</span></span>

<span data-ttu-id="67e50-105">Les serveurs DLL sont chargés, par défaut, dans leur propre processus de substitution.</span><span class="sxs-lookup"><span data-stu-id="67e50-105">DLL servers are loaded, by default, into their own surrogate process.</span></span> <span data-ttu-id="67e50-106">Pour charger d’autres serveurs DLL dans un substitut existant afin qu’il prenne en charge plusieurs serveurs DLL, deux conditions sont requises :</span><span class="sxs-lookup"><span data-stu-id="67e50-106">To load other DLL servers into an existing surrogate so that it supports more than one DLL server, there are two requirements:</span></span>

-   <span data-ttu-id="67e50-107">Les serveurs DLL doivent avoir la même valeur AppID.</span><span class="sxs-lookup"><span data-stu-id="67e50-107">The DLL servers must have the same AppID value.</span></span>
-   <span data-ttu-id="67e50-108">Le contexte de sécurité des serveurs DLL doit être le même.</span><span class="sxs-lookup"><span data-stu-id="67e50-108">The security context of the DLL servers must be the same.</span></span>

<span data-ttu-id="67e50-109">Si deux serveurs DLL doivent être lancés sous différentes identités de sécurité, ils doivent être dans des substituts différents, que leurs AppID correspondent.</span><span class="sxs-lookup"><span data-stu-id="67e50-109">If two DLL servers are to be launched under different security identities, they must be in different surrogates, whether their AppIDs match.</span></span>

<span data-ttu-id="67e50-110">Voici un exemple d’administration du partage de substitution avec les AppID :</span><span class="sxs-lookup"><span data-stu-id="67e50-110">Following is an example of administering surrogate sharing with AppIDs:</span></span>

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

<span data-ttu-id="67e50-111">Les deux CLSID des composants DLL comp1.dll et comp2.dll ont été configurés pour partager une AppID.</span><span class="sxs-lookup"><span data-stu-id="67e50-111">The two CLSIDs for DLL components comp1.dll and comp2.dll have been configured to share an AppID.</span></span> <span data-ttu-id="67e50-112">La clé [AppID](appid-key.md) spécifie que le serveur dll peut être chargé dans un substitut en spécifiant la valeur [DllSurrogate](dllsurrogate.md) .</span><span class="sxs-lookup"><span data-stu-id="67e50-112">The [AppID](appid-key.md) key specifies that the DLL server can be loaded in a surrogate by specifying the [DllSurrogate](dllsurrogate.md) value.</span></span> <span data-ttu-id="67e50-113">Dans cet exemple, la valeur **DllSurrogate** est une chaîne vide, ce qui indique que l’implémentation système par défaut du substitut de la dll doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="67e50-113">In this example, the **DllSurrogate** value is an empty string, indicating that the default system implementation of the DLL surrogate should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67e50-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67e50-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67e50-115">Configuration requise du serveur DLL</span><span class="sxs-lookup"><span data-stu-id="67e50-115">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="67e50-116">Inscription du serveur DLL pour l’activation du remplacement</span><span class="sxs-lookup"><span data-stu-id="67e50-116">Registering the DLL Server for Surrogate Activation</span></span>](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




