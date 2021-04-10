---
description: L’architecture Windows Sockets 2 (Winsock) est conforme à l’architecture WOSA (Windows Open System Architecture).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Architecture Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114299"
---
# <a name="windows-sockets-2-architecture"></a><span data-ttu-id="400f8-103">Architecture Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="400f8-103">Windows Sockets 2 Architecture</span></span>

<span data-ttu-id="400f8-104">L’architecture Windows Sockets 2 est conforme à l’architecture WOSA (Windows Open System Architecture), comme illustré ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="400f8-104">The Windows Sockets 2 architecture is compliant with the Windows Open System Architecture (WOSA), as illustrated below:</span></span>

![architecture Windows Sockets 2](images/ovrvw2-1.png)

<span data-ttu-id="400f8-106">Winsock définit une interface de fournisseur de services (SPI) standard entre l’interface de programmation d’applications (API), avec ses fonctions exportées à partir de WS2 \_32.dll et les piles de protocole.</span><span class="sxs-lookup"><span data-stu-id="400f8-106">Winsock defines a standard service provider interface (SPI) between the application programming interface (API), with its functions exported from WS2\_32.dll and the protocol stacks.</span></span> <span data-ttu-id="400f8-107">Par conséquent, la prise en charge de Winsock n’est pas limitée aux piles de protocole TCP/IP, comme c’est le cas pour Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="400f8-107">Consequently, Winsock support is not limited to TCP/IP protocol stacks as is the case for Windows Sockets 1.1.</span></span>

<span data-ttu-id="400f8-108">Avec l’architecture Windows Sockets 2, il n’est pas nécessaire ou souhaitable pour les fournisseurs de pile de fournir leur propre implémentation de WS2 \_32.dll, car un même WS2 \_32.dll doit fonctionner sur toutes les piles.</span><span class="sxs-lookup"><span data-stu-id="400f8-108">With the Windows Sockets 2 architecture, it is not necessary or desirable, for stack vendors to supply their own implementation of WS2\_32.dll, since a single WS2\_32.dll must work across all stacks.</span></span> <span data-ttu-id="400f8-109">Les \_32.dll WS2 et les shims de compatibilité doivent être affichés de la même façon qu’un composant du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="400f8-109">The WS2\_32.dll and compatibility shims should be viewed in the same way as an operating system component.</span></span>

 

 



