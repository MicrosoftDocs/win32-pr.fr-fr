---
description: L’installation d’un nouveau fournisseur de services est spécifique aux appareils et au système d’exploitation, donc les détails ne sont pas abordés dans le cadre de ce kit de développement logiciel (SDK).
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Installation et initialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534736"
---
# <a name="installation-and-initialization"></a><span data-ttu-id="fb1f9-103">Installation et initialisation</span><span class="sxs-lookup"><span data-stu-id="fb1f9-103">Installation and Initialization</span></span>

<span data-ttu-id="fb1f9-104">L’installation d’un nouveau fournisseur de services est spécifique aux appareils et au système d’exploitation, donc les détails ne sont pas abordés dans le cadre de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="fb1f9-104">Installation of a new service provider is highly device- and operating-system-specific, so the details are outside the scope of this SDK.</span></span> <span data-ttu-id="fb1f9-105">En règle générale, l’objectif de l’installation est la configuration du fournisseur de services pour l’environnement de communication actuel.</span><span class="sxs-lookup"><span data-stu-id="fb1f9-105">Generally speaking, the goal of installation is configuration of the service provider for the current communications environment.</span></span> <span data-ttu-id="fb1f9-106">Cela implique généralement les entrées de Registre et le paramètre des dépendances de service.</span><span class="sxs-lookup"><span data-stu-id="fb1f9-106">This usually involves registry entries and the setting of service dependencies.</span></span>

<span data-ttu-id="fb1f9-107">L’initialisation d’un fournisseur de services de téléphonie commence par la négociation de version.</span><span class="sxs-lookup"><span data-stu-id="fb1f9-107">Initialization of a telephony service provider starts with version negotiation.</span></span> <span data-ttu-id="fb1f9-108">Consultez [gestion des versions TSPI](tspi-versioning.md) pour une discussion sur la négociation de versions et la version actuelle.</span><span class="sxs-lookup"><span data-stu-id="fb1f9-108">See [TSPI Versioning](tspi-versioning.md) for a discussion of version negotiation and current version.</span></span>

<span data-ttu-id="fb1f9-109">L’interface TAPI appelle ensuite [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), qui transmet au fournisseur un pointeur vers une fonction de rappel utilisée pour signaler la progression des fonctions asynchrones.</span><span class="sxs-lookup"><span data-stu-id="fb1f9-109">TAPI then calls [**TSPI\_providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), which passes the provider a pointer to a callback function used to report on asynchronous functions progress.</span></span> <span data-ttu-id="fb1f9-110">Le TSP renvoie un nombre de lignes et d’appareils téléphoniques associés à l’identificateur d’appareil actuel.</span><span class="sxs-lookup"><span data-stu-id="fb1f9-110">The TSP returns a count of line and phone devices associated with the current device identifier.</span></span>

<span data-ttu-id="fb1f9-111">En règle générale, l’étape suivante est l’inventaire des ressources, effectué par TAPI appelant [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) et [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span><span class="sxs-lookup"><span data-stu-id="fb1f9-111">Typically, the next step will be resource inventory, conducted by TAPI invoking [**TSPI\_lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) and [**TSPI\_lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span></span> <span data-ttu-id="fb1f9-112">Le fournisseur de services est supposé remplir les éléments des structures de données impliquées qui se rapportent aux fonctionnalités de l’appareil et de la session qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="fb1f9-112">The service provider is expected to fill in those elements of the data structures involved that pertain to device and session capabilities it supports.</span></span>

<span data-ttu-id="fb1f9-113">L’interface TAPI collecte des informations à partir des différentes applications relatives aux exigences de notification d’événement et indique au TSP d’utiliser [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) pour indiquer les types de médias à détecter pour une ligne et [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) pour indiquer les événements de ligne et d’adresse qui doivent être signalés.</span><span class="sxs-lookup"><span data-stu-id="fb1f9-113">TAPI collects information from the various applications concerning event notification requirements, and instructs the TSP using [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) to indicate which media types to detect for a line and [**TSPI\_lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) to indicate which line and address events should be reported.</span></span>

 

 
