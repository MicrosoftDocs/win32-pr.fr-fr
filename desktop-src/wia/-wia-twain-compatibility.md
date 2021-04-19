---
description: WIA fournit une couche de compatibilité TWAIN qui permet aux applications compatibles TWAIN de communiquer avec les périphériques WIA (Windows Image Acquisition).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilité avec TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516675"
---
# <a name="twain-compatibility"></a><span data-ttu-id="4edf6-103">Compatibilité avec TWAIN</span><span class="sxs-lookup"><span data-stu-id="4edf6-103">TWAIN Compatibility</span></span>

<span data-ttu-id="4edf6-104">WIA fournit une couche de compatibilité TWAIN qui permet aux applications compatibles TWAIN de communiquer avec les périphériques WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="4edf6-104">WIA provides a TWAIN compatibility layer that allows TWAIN-aware applications to communicate with Windows Image Acquisition (WIA) devices.</span></span> <span data-ttu-id="4edf6-105">Les applications compatibles TWAIN n’ont pas un accès complet à la fonctionnalité WIA.</span><span class="sxs-lookup"><span data-stu-id="4edf6-105">TWAIN-aware applications do not have full access to WIA functionality.</span></span> <span data-ttu-id="4edf6-106">Par exemple, une application ne peut pas supprimer l’interface utilisateur à l’aide de la couche de compatibilité TWAIN.</span><span class="sxs-lookup"><span data-stu-id="4edf6-106">For example, an application cannot suppress the user interface using the TWAIN compatibility layer.</span></span>

<span data-ttu-id="4edf6-107">Les périphériques WIA apparaissent deux fois pour une application qui est consciente de WIA et TWAIN : une fois par le biais d’une communication WIA normale et une fois par le biais de la couche de compatibilité TWAIN.</span><span class="sxs-lookup"><span data-stu-id="4edf6-107">WIA devices appear twice to an application that is aware of both WIA and TWAIN: once through normal WIA communication, and once through the TWAIN compatibility layer.</span></span> <span data-ttu-id="4edf6-108">Pour éviter de répertorier deux fois un appareil WIA, une application qui prend en charge WIA et TWAIN doit filtrer les appareils WIA qui passent par la couche de compatibilité TWAIN.</span><span class="sxs-lookup"><span data-stu-id="4edf6-108">To avoid listing a WIA device twice, an application that is aware of both WIA and TWAIN must filter out the WIA devices that come through the TWAIN compatibility layer.</span></span> <span data-ttu-id="4edf6-109">Tous les appareils WIA qui passent par la couche de compatibilité TWAIN ont un préfixe « WIA ». il est donc facile de les filtrer.</span><span class="sxs-lookup"><span data-stu-id="4edf6-109">All WIA devices that come through the TWAIN compatibility layer have "WIA-" as a prefix, so it is easy to filter them.</span></span>

 

 



