---
description: La qualité de service (QoS) est implémentée dans Windows par le biais de différents composants QoS pris en charge sur Windows Server 2003, Windows XP et Windows 2000.
ms.assetid: e55b085f-6f72-4aa4-a8b0-b7609b9010dc
title: Qualité de service dans le SPI Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87d37f2e30e0a4fb296fc340353e2f4d85b5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527408"
---
# <a name="quality-of-service-in-the-windows-sockets-2-spi"></a><span data-ttu-id="44693-103">Qualité de service dans le SPI Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="44693-103">Quality of Service in the Windows Sockets 2 SPI</span></span>

<span data-ttu-id="44693-104">La qualité de service (QoS) est implémentée dans Windows par le biais de différents composants QoS pris en charge sur Windows Server 2003, Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="44693-104">Quality of Service (QoS) is implemented in Windows through various QoS components supported on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="44693-105">Une explication détaillée de la QoS et de ses composants se trouve dans une section consacrée à la qualité de service, qui se trouve dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="44693-105">A detailed explanation of QoS and its components is located in a section dedicated to Quality of Service, located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="44693-106">Chaque composant QoS et le rôle qu’il joue dans l’implémentation de QoS sont expliqués dans cette section QoS, avec des conseils supplémentaires fournis pour l’implémentation d’applications et de services compatibles QoS.</span><span class="sxs-lookup"><span data-stu-id="44693-106">Each QoS component, and the role it plays in the QoS implementation, is explained in this QoS section, with additional guidance provided for the implementation of QoS-enabled applications and services.</span></span> <span data-ttu-id="44693-107">Pour plus d’informations, consultez la section [qualité de service (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="44693-107">Please see the [Quality of Service (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) section of the Windows SDK for more detailed information.</span></span>

<span data-ttu-id="44693-108">Cette section décrit les fonctionnalités de qualité de service disponibles pour les développeurs Winsock.</span><span class="sxs-lookup"><span data-stu-id="44693-108">This section describes Quality of Service capabilities available to Winsock developers.</span></span> <span data-ttu-id="44693-109">La liste suivante décrit les rubriques de cette section :</span><span class="sxs-lookup"><span data-stu-id="44693-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="44693-110">Modèle d’utilisation</span><span class="sxs-lookup"><span data-stu-id="44693-110">Usage Model</span></span>](usage-model-2.md)
-   [<span data-ttu-id="44693-111">Mises à jour QoS</span><span class="sxs-lookup"><span data-stu-id="44693-111">QoS Updates</span></span>](qos-updates-2.md)
-   [<span data-ttu-id="44693-112">Valeurs par défaut dans l’index SPI</span><span class="sxs-lookup"><span data-stu-id="44693-112">Default Values in the SPI</span></span>](default-values-in-the-spi-2.md)
-   [<span data-ttu-id="44693-113">Modèles QoS dans le SPI</span><span class="sxs-lookup"><span data-stu-id="44693-113">QoS Templates in the SPI</span></span>](qos-templates-in-the-spi-2.md)

## <a name="related-topics"></a><span data-ttu-id="44693-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44693-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44693-115">Quality of Service (QoS)</span><span class="sxs-lookup"><span data-stu-id="44693-115">Quality of Service (QoS)</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> <dt>

<span data-ttu-id="44693-116">[Qu’est-ce que la qualité de service ?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="44693-116">[What Is QoS?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="44693-117">Extension Winsock ATM QoS</span><span class="sxs-lookup"><span data-stu-id="44693-117">Winsock ATM QoS Extension</span></span>](winsock-atm-qos-extension.md)
</dt> <dt>

[<span data-ttu-id="44693-118">**IOCTL Winsock**</span><span class="sxs-lookup"><span data-stu-id="44693-118">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
