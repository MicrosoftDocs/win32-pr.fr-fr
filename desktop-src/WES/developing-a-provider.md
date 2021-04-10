---
title: Développement d’un fournisseur
description: Pour écrire les événements que vous définissez dans votre manifeste, vous utilisez les fonctions incluses dans l’API de suivi d’événements (ETW). Pour plus d’informations sur l’écriture d’un fournisseur, consultez fourniture d’événements.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102205"
---
# <a name="developing-a-provider"></a><span data-ttu-id="6e772-104">Développement d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="6e772-104">Developing a Provider</span></span>

<span data-ttu-id="6e772-105">Pour écrire les événements que vous définissez dans votre manifeste, vous utilisez les fonctions incluses dans l’API de [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="6e772-105">To write the events that you define in your manifest, you use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span> <span data-ttu-id="6e772-106">Pour plus d’informations sur l’écriture d’un fournisseur, consultez [fourniture d’événements](/windows/desktop/ETW/providing-events).</span><span class="sxs-lookup"><span data-stu-id="6e772-106">For details on writing a provider, see [Providing Events](/windows/desktop/ETW/providing-events).</span></span>

<span data-ttu-id="6e772-107">Après avoir écrit le fournisseur, utilisez l’outil WevtUtil.exe pour inscrire le fournisseur et le schéma.</span><span class="sxs-lookup"><span data-stu-id="6e772-107">After writing the provider, use the WevtUtil.exe tool to register the provider and schema.</span></span> <span data-ttu-id="6e772-108">Pour plus d’informations sur l’utilisation de WevtUtil, consultez [outils du journal des événements Windows](windows-event-log-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6e772-108">For details on using WevtUtil, see [Windows Event Log Tools](windows-event-log-tools.md).</span></span> <span data-ttu-id="6e772-109">L’exemple suivant montre comment utiliser WevtUtil pour inscrire un fournisseur et supprimer l’inscription.</span><span class="sxs-lookup"><span data-stu-id="6e772-109">The following shows how to use WevtUtil to register a provider and to remove the registration.</span></span>


```cmd
wevtutil im provider.man

wevtutil um provider.man
```