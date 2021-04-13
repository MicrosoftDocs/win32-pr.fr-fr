---
description: À compter des fournisseurs de services de téléphonie Windows 2000 qui négocient une version de 3,0 ou ultérieure doit avoir un fournisseur de services de média correspondant.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Communication du fournisseur de services de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a50ec6a4fb96a86ceab3a302b138ee72d6c61b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321566"
---
# <a name="media-service-provider-communication"></a><span data-ttu-id="0ab23-103">Communication du fournisseur de services de média</span><span class="sxs-lookup"><span data-stu-id="0ab23-103">Media Service Provider Communication</span></span>

<span data-ttu-id="0ab23-104">À compter des fournisseurs de services de téléphonie Windows 2000 qui négocient une version de 3,0 ou ultérieure doit avoir un fournisseur de services de média correspondant.</span><span class="sxs-lookup"><span data-stu-id="0ab23-104">Starting with Windows 2000 telephony service providers that negotiate a version of 3.0 or later must have a matching media service provider.</span></span> <span data-ttu-id="0ab23-105">La Division précise des responsabilités opérationnelles dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="0ab23-105">The precise division of operational responsibilities is implementation dependent.</span></span> <span data-ttu-id="0ab23-106">Par exemple, un TSP peut utiliser le MSP correspondant pour effectuer la détermination du type de média sur une session entrante.</span><span class="sxs-lookup"><span data-stu-id="0ab23-106">For example, a TSP might use the matching MSP to perform media type determination on an incoming session.</span></span> <span data-ttu-id="0ab23-107">Toutefois, le TSP doit se conformer au TSPI, ce qui signifie obtenir cette détermination auprès du MSP et le signaler à TAPI.</span><span class="sxs-lookup"><span data-stu-id="0ab23-107">However, the TSP must conform to the TSPI, which means getting that determination from the MSP and reporting it to TAPI.</span></span>

<span data-ttu-id="0ab23-108">TSPI fournit les fonctions et messages suivants pour autoriser une connexion virtuelle entre un TSP et un MSP :</span><span class="sxs-lookup"><span data-stu-id="0ab23-108">TSPI provides the following functions and messages to allow a virtual connection between a TSP and an MSP:</span></span>

-   [<span data-ttu-id="0ab23-109">**TSPI \_ lineCloseMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="0ab23-109">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [<span data-ttu-id="0ab23-110">**TSPI \_ lineCreateMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="0ab23-110">**TSPI\_lineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [<span data-ttu-id="0ab23-111">**TSPI \_ lineMSPIdentify**</span><span class="sxs-lookup"><span data-stu-id="0ab23-111">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [<span data-ttu-id="0ab23-112">**TSPI \_ lineReceiveMSPData**</span><span class="sxs-lookup"><span data-stu-id="0ab23-112">**TSPI\_lineReceiveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [<span data-ttu-id="0ab23-113">**QOSINFO de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="0ab23-113">**LINE\_QOSINFO**</span></span>](line-qosinfo.md)
-   [<span data-ttu-id="0ab23-114">**SENDMSPDATA de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="0ab23-114">**LINE\_SENDMSPDATA**</span></span>](line-sendmspdata.md)

 

 
