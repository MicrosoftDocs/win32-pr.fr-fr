---
description: Les outils de développement WSDAPI inclus dans le SDK Windows (WSD CodeGen, l’hôte de débogage WSD et le client de débogage WSD) permettent aux développeurs de créer et de déboguer des périphériques et des clients WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Outils de développement WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519607"
---
# <a name="wsdapi-development-tools"></a><span data-ttu-id="36e8f-103">Outils de développement WSDAPI</span><span class="sxs-lookup"><span data-stu-id="36e8f-103">WSDAPI Development Tools</span></span>

<span data-ttu-id="36e8f-104">Les outils de développement WSDAPI inclus dans le SDK Windows (WSD CodeGen, l’hôte de débogage WSD et le client de débogage WSD) permettent aux développeurs de créer et de déboguer des périphériques et des clients WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="36e8f-104">The WSDAPI development tools included in the Windows SDK (WSD CodeGen, WSD Debug Host, and WSD Debug Client) enable developers to create and debug WSDAPI-based clients and devices.</span></span> <span data-ttu-id="36e8f-105">Le code source de ces outils n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="36e8f-105">The source code for these tools is not available.</span></span> <span data-ttu-id="36e8f-106">Les outils du kit de développement logiciel se trouvent dans le répertoire suivant : <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="36e8f-106">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="36e8f-107">WSD CodeGen (wsdcodegen.exe) convertit un contrat WSDL en code C++ généré, que les développeurs peuvent appeler directement dans.</span><span class="sxs-lookup"><span data-stu-id="36e8f-107">WSD CodeGen (wsdcodegen.exe) converts a WSDL contract into generated C++ code, which developers can call directly into.</span></span> <span data-ttu-id="36e8f-108">Il gère la sérialisation des données et la représentation filaire afin que les développeurs puissent se concentrer sur la conception d’applications.</span><span class="sxs-lookup"><span data-stu-id="36e8f-108">It handles the data serialization and wire representation so developers can focus on designing applications.</span></span> <span data-ttu-id="36e8f-109">Pour plus d’informations sur WSD CodeGen, consultez [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="36e8f-109">For more information about WSD CodeGen, see [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="36e8f-110">Cet outil est disponible dans le kit de développement logiciel (SDK) Microsoft Windows et dans le kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="36e8f-110">This tool is available in the Microsoft Windows Software Development Kit (SDK) and in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="36e8f-111">Les outils de débogage de l’hôte de débogage WSD (wsddebug \_host.exe) et du client de débogage WSD (wsddebug \_client.exe) aident les développeurs à déboguer leurs clients et hôtes.</span><span class="sxs-lookup"><span data-stu-id="36e8f-111">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools help developers debug their clients and hosts.</span></span> <span data-ttu-id="36e8f-112">Ces outils peuvent être utilisés pour vérifier et inspecter les WS-Discovery et le trafic d’échange de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="36e8f-112">These tools can be used to verify and inspect WS-Discovery and metadata exchange traffic.</span></span> <span data-ttu-id="36e8f-113">Pour plus d’informations sur l’hôte de débogage WSD et le client de débogage WSD, consultez [outils de débogage](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="36e8f-113">For more information about WSD Debug Host and WSD Debug Client, see [Debugging Tools](debugging-tools.md).</span></span> <span data-ttu-id="36e8f-114">Ces outils sont disponibles uniquement dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="36e8f-114">These tools are available only in the Windows SDK.</span></span>

<span data-ttu-id="36e8f-115">Il existe un outil de développement supplémentaire, nommé [wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), qui est disponible uniquement dans le kit WDK.</span><span class="sxs-lookup"><span data-stu-id="36e8f-115">There is an additional development tool, named [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), that is available only in the WDK.</span></span> <span data-ttu-id="36e8f-116">Cet outil est utilisé pour tester les méthodes de service, MTOM (Message Transmission Optimization Mechanism), les pièces jointes ou WS-Eventing.</span><span class="sxs-lookup"><span data-stu-id="36e8f-116">This tool is used for testing service methods, Message Transmission Optimization Mechanism (MTOM), attachments or WS-Eventing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36e8f-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36e8f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36e8f-118">Développement d’applications WSD sur Windows</span><span class="sxs-lookup"><span data-stu-id="36e8f-118">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="36e8f-119">Générateur de code des services Web sur les appareils</span><span class="sxs-lookup"><span data-stu-id="36e8f-119">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="36e8f-120">Outil d’interopérabilité de base WSDAPI (WSDBIT)</span><span class="sxs-lookup"><span data-stu-id="36e8f-120">WSDAPI Basic Interoperability Tool (WSDBIT)</span></span>](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[<span data-ttu-id="36e8f-121">Outils de débogage</span><span class="sxs-lookup"><span data-stu-id="36e8f-121">Debugging Tools</span></span>](debugging-tools.md)
</dt> </dl>

 

 



