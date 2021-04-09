---
title: Entrées de Registre (COM)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 'En savoir plus sur : entrées de Registre (COM)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111454"
---
# <a name="registry-entries-com"></a><span data-ttu-id="9f10f-103">Entrées de Registre (COM)</span><span class="sxs-lookup"><span data-stu-id="9f10f-103">Registry Entries (COM)</span></span>

<span data-ttu-id="9f10f-104">Les valeurs de Registre dans les clés de Registre suivantes contrôlent les aspects de la fonctionnalité de COM :</span><span class="sxs-lookup"><span data-stu-id="9f10f-104">Registry values in the following registry keys control aspects of the functionality of COM:</span></span>

-   [<span data-ttu-id="9f10f-105">**HKEY \_ local \_ machine \\ classes de logiciels \\**</span><span class="sxs-lookup"><span data-stu-id="9f10f-105">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**</span></span>](hkey-local-machine-software-classes.md)
-   [<span data-ttu-id="9f10f-106">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE**</span><span class="sxs-lookup"><span data-stu-id="9f10f-106">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Ole**</span></span>](hkey-local-machine-software-microsoft-ole.md)
-   [<span data-ttu-id="9f10f-107">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="9f10f-107">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

<span data-ttu-id="9f10f-108">À compter de Windows Server 2003, COM utilise uniquement le jeton de processus actuel pour décider de la ruche de Registre à laquelle accéder, et non le jeton de thread.</span><span class="sxs-lookup"><span data-stu-id="9f10f-108">As of Windows Server 2003, COM uses only the current process token to decide which registry hive to access, not the thread token.</span></span> <span data-ttu-id="9f10f-109">Si COM n’est pas en mesure d’accéder à la ruche du Registre du profil utilisateur, il accède à la ruche du système de l' **\_ \_ ordinateur \\ local HKEY** .</span><span class="sxs-lookup"><span data-stu-id="9f10f-109">If COM is not able to access the user profile registry hive, it will access the **HKEY\_LOCAL\_MACHINE\\System** hive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f10f-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9f10f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f10f-111">Registre</span><span class="sxs-lookup"><span data-stu-id="9f10f-111">Registry</span></span>](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
