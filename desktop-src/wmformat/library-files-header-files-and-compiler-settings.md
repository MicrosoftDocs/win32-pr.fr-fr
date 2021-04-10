---
title: Fichiers de bibliothèque, fichiers d’en-tête et paramètres du compilateur
description: Fichiers de bibliothèque, fichiers d’en-tête et paramètres du compilateur
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- Windows Media Format SDK, fichiers de bibliothèque DRM
- Windows Media Format SDK, fichiers de bibliothèque
- Windows Media Format SDK, fichiers d’en-tête DRM
- Windows Media Format SDK, fichiers d’en-tête
- Windows Media Format SDK, paramètres du compilateur DRM
- Windows Media Format SDK, paramètres du compilateur
- gestion des droits numériques (DRM), fichiers de bibliothèque
- DRM (gestion des droits numériques), fichiers de bibliothèque
- gestion des droits numériques (DRM), fichiers d’en-tête
- DRM (gestion des droits numériques), fichiers d’en-tête
- gestion des droits numériques (DRM), paramètres du compilateur
- DRM (gestion des droits numériques), paramètres du compilateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100740"
---
# <a name="library-files-header-files-and-compiler-settings"></a><span data-ttu-id="b11c7-115">Fichiers de bibliothèque, fichiers d’en-tête et paramètres du compilateur</span><span class="sxs-lookup"><span data-stu-id="b11c7-115">Library Files, Header Files, and Compiler Settings</span></span>

<span data-ttu-id="b11c7-116">Les composants de programmation des API étendues du client Windows Media DRM sont définis dans le fichier d’en-tête wmdrmsdk. h et implémentés dans les bibliothèques wmdrmsdk. lib et mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b11c7-116">The programming components of the Windows Media DRM Client Extended APIs are defined in the wmdrmsdk.h header file, and implemented in the wmdrmsdk.lib and mfuuid.lib libraries.</span></span>

<span data-ttu-id="b11c7-117">Certaines fonctionnalités des API étendues du client Windows Media DRM requièrent que vous obteniez une bibliothèque protégée de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b11c7-117">Some of the functionality of the Windows Media DRM Client Extended APIs requires that you obtain a protected library from Microsoft.</span></span> <span data-ttu-id="b11c7-118">Cette bibliothèque, appelée bibliothèque stub dans cette documentation, est spécifique au destinataire et spécifie le niveau de sécurité de l’application pour vos applications.</span><span class="sxs-lookup"><span data-stu-id="b11c7-118">This library, called the stub library in this documentation, is specific to the recipient and specifies the application security level for your applications.</span></span> <span data-ttu-id="b11c7-119">La bibliothèque stub remplace wmdrmsdk. lib ; vous ne devez jamais établir de liaison avec les deux.</span><span class="sxs-lookup"><span data-stu-id="b11c7-119">The stub library replaces wmdrmsdk.lib; you should never link to both.</span></span>

<span data-ttu-id="b11c7-120">**Remarque** La bibliothèque de stubs DRM est distincte de la bibliothèque de stubs utilisée par le reste du kit de développement logiciel (SDK) du format Windows Media, mais elle est autorisée à l’aide de la même méthode.</span><span class="sxs-lookup"><span data-stu-id="b11c7-120">**Note** The DRM stub library is separate from the stub library used by the rest of the Windows Media Format SDK but is licensed using the same method.</span></span>

<span data-ttu-id="b11c7-121">**Remarque** La bibliothèque de stubs DRM doit être liée à votre application après le fichier de bibliothèque Msvcrt. lib pour éviter les erreurs de l’éditeur de liens.</span><span class="sxs-lookup"><span data-stu-id="b11c7-121">**Note** The DRM stub library must be linked into your application after the library file msvcrt.lib to avoid linker errors.</span></span>

<span data-ttu-id="b11c7-122">La bibliothèque stub contient un certificat incorporé qui peut être révoqué par Microsoft si vous ne respectez pas les conditions générales du contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="b11c7-122">The stub library contains an embedded certificate which can be revoked by Microsoft if you fail to comply with the terms and conditions of the license agreement.</span></span>

<span data-ttu-id="b11c7-123">Les méthodes spécifiques qui requièrent la bibliothèque stub sont étiquetées dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="b11c7-123">Specific methods that require the stub library are labeled in the documentation.</span></span> <span data-ttu-id="b11c7-124">Si vous essayez d’utiliser une telle méthode sans établir de liaison avec la bibliothèque de stubs, elle renverra une erreur de type STUBLIB de la bibliothèque de multiservice (DRM) NS \_ E \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b11c7-124">If you try to use such a method without linking to the stub library, it will return an NS\_E\_DRM\_STUBLIB\_REQUIRED error.</span></span>

<span data-ttu-id="b11c7-125">Le sous-système DRM ne peut pas être utilisé dans une version Debug.</span><span class="sxs-lookup"><span data-stu-id="b11c7-125">The DRM subsystem can not be used in a debug build.</span></span> <span data-ttu-id="b11c7-126">Si cette tentative est effectuée, les méthodes de l’API retournent l’erreur de débogage de l’interface de ligne de service (DRM) NS \_ E \_ \_ \_ non \_ autorisée.</span><span class="sxs-lookup"><span data-stu-id="b11c7-126">If this is attempted, methods of the API will return the NS\_E\_DRM\_DEBUGGING\_NOT\_ALLOWED error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b11c7-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b11c7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b11c7-128">**Prise en main**</span><span class="sxs-lookup"><span data-stu-id="b11c7-128">**Getting Started**</span></span>](drm-getting-started.md)
</dt> <dt>

[<span data-ttu-id="b11c7-129">**Fichiers de bibliothèque et paramètres du compilateur**</span><span class="sxs-lookup"><span data-stu-id="b11c7-129">**Library Files and Compiler Settings**</span></span>](library-files-and-compiler-settings.md)
</dt> <dt>

[<span data-ttu-id="b11c7-130">**Obtention de la bibliothèque DRM requise**</span><span class="sxs-lookup"><span data-stu-id="b11c7-130">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




