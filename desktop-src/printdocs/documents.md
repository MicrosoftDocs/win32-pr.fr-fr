---
description: Cette section décrit les technologies de document qui sont prises en charge par Microsoft Windows.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: Documents XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa96324014d00a2a9fc106347fbeafe9842dedd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545113"
---
# <a name="xps-documents"></a><span data-ttu-id="e3b9c-103">Documents XPS</span><span class="sxs-lookup"><span data-stu-id="e3b9c-103">XPS Documents</span></span>

<span data-ttu-id="e3b9c-104">Cette section décrit les technologies de document qui sont prises en charge par Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-104">This section describes the document technologies that are supported by Microsoft Windows.</span></span>

-   [<span data-ttu-id="e3b9c-105">Choix d’une technologie de document</span><span class="sxs-lookup"><span data-stu-id="e3b9c-105">Choosing a Document Technology</span></span>](#choosing-a-document-technology)
-   [<span data-ttu-id="e3b9c-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e3b9c-106">In This Section</span></span>](#in-this-section)
-   [<span data-ttu-id="e3b9c-107">Outils de document XPS</span><span class="sxs-lookup"><span data-stu-id="e3b9c-107">XPS Document Tools</span></span>](#xps-document-tools)
-   [<span data-ttu-id="e3b9c-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3b9c-108">Related topics</span></span>](#related-topics)


## <a name="choosing-a-document-technology"></a><span data-ttu-id="e3b9c-109">Choix d’une technologie de document</span><span class="sxs-lookup"><span data-stu-id="e3b9c-109">Choosing a Document Technology</span></span>

<span data-ttu-id="e3b9c-110">Microsoft fournit plusieurs technologies de documents différentes pour prendre en charge une grande variété d’applications de document :</span><span class="sxs-lookup"><span data-stu-id="e3b9c-110">Microsoft provides several different document technologies to support a variety of document applications:</span></span>

-   <span data-ttu-id="e3b9c-111">**XPS et OpenXPS**</span><span class="sxs-lookup"><span data-stu-id="e3b9c-111">**XPS and OpenXPS**</span></span>

    <span data-ttu-id="e3b9c-112">XPS et OpenXPS sont pris en charge dans Windows 8 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-112">XPS and OpenXPS are supported in Windows 8 and later versions of Windows.</span></span> <span data-ttu-id="e3b9c-113">Consultez le diagramme précédent pour déterminer le scénario d’utilisation approprié pour XPS et OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-113">See the preceding diagram to determine the correct usage scenario for XPS and OpenXPS.</span></span> <span data-ttu-id="e3b9c-114">Pour plus d’informations sur ces technologies de documents, consultez [Open XML Paper Specification (en anglais) (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-114">For more information about these document technologies, see [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span></span>

    <span data-ttu-id="e3b9c-115">Dans le cas de l’utilisation de OpenXPS avec Windows 8 et Windows Server 2012, la prise en charge est fournie uniquement via l' [API de document XPS](documents-xps.md) .</span><span class="sxs-lookup"><span data-stu-id="e3b9c-115">In the case of using OpenXPS with Windows 8 and Windows Server 2012, support is only provided via the [XPS Document API](documents-xps.md)</span></span>

    <span data-ttu-id="e3b9c-116">Si vous devez effectuer une conversion entre Microsoft XPS (MSXPS) et OpenXPS, Microsoft a fourni un outil (XPSConverter.exe) qui vous permet de convertir des documents au format OpenXPS et vice versa.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-116">If you need to convert between Microsoft XPS (MSXPS) and OpenXPS, then Microsoft has provided a tool (XPSConverter.exe) that allows you to convert MSXPS-formatted documents to the OpenXPS format and vice versa.</span></span> <span data-ttu-id="e3b9c-117">L’outil fait partie du kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-117">The tool is part of the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="e3b9c-118">Pour télécharger le kit WDK, consultez [Comment obtenir le kit WDK](/windows-hardware/drivers/download-the-wdk).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-118">To download the WDK, see [How to get the WDK](/windows-hardware/drivers/download-the-wdk).</span></span>

    <span data-ttu-id="e3b9c-119">Pour plus d’informations sur OpenXPS et Windows 8, consultez [prise en charge de OpenXPS dans Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-119">And for more information about OpenXPS and Windows 8, see [OpenXPS Support in Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span></span>

-   <span data-ttu-id="e3b9c-120">**API de document XPS**</span><span class="sxs-lookup"><span data-stu-id="e3b9c-120">**XPS Document API**</span></span>

    <span data-ttu-id="e3b9c-121">L’API de document XPS est une API Windows native qui prend en charge le modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-121">The XPS Document API is a native Windows API that supports the XPS OM.</span></span> <span data-ttu-id="e3b9c-122">L’API de document XPS a été introduite dans Windows 7 et peut être utilisée dans les programmes en mode utilisateur et les pilotes d’imprimante XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-122">The XPS Document API was introduced in Windows 7 and can be used in user-mode programs and XPSDrv printer drivers.</span></span>

    <span data-ttu-id="e3b9c-123">Pour plus d’informations, consultez l’API de document XPS et l' [API de signature numérique XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-123">For more information, see the XPS Document API, and [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

    <span data-ttu-id="e3b9c-124">\*L’API de document XPS est également prise en charge dans Windows Vista avec Service Pack 2 (SP2) avec la mise à jour de plateforme pour Windows Vista et Windows Server 2008 avec SP2 à l’aide de la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-124">\*The XPS Document API is also supported in Windows Vista with Service Pack 2 (SP2) with the Platform Update for Windows Vista and Windows Server 2008 with SP2 using the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="e3b9c-125">Pour plus d’informations sur la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008, consultez [mise à jour de la plateforme pour Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal) .</span><span class="sxs-lookup"><span data-stu-id="e3b9c-125">For more information about the Platform Update for Windows Vista or the Platform Update for Windows Server 2008, see [Platform Update for Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span></span>

-   <span data-ttu-id="e3b9c-126">**.NET Framework**</span><span class="sxs-lookup"><span data-stu-id="e3b9c-126">**.NET Framework**</span></span>

    <span data-ttu-id="e3b9c-127">.NET Framework fournit une prise en charge des documents XPS pour les programmes en mode utilisateur et de code géré.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-127">.NET Framework provides XPS document support to user-mode, managed-code programs.</span></span>

    <span data-ttu-id="e3b9c-128">.NET Framework 3,0 est pris en charge sur Windows XP avec Service Pack 2 (SP2) et les versions ultérieures des systèmes d’exploitation clients Windows, et sur Windows Server 2003 avec Service Pack 2 (SP2) et les versions ultérieures des systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-128">.NET Framework 3.0 is supported on Windows XP with Service Pack 2 (SP2) and later versions of Windows client operating systems, and on Windows Server 2003 with Service Pack 2 (SP2) and later versions of Windows server operating systems.</span></span>

    <span data-ttu-id="e3b9c-129">.NET Framework 3,5 est pris en charge sur les versions Windows XP des systèmes d’exploitation clients Windows et sur Windows Server 2003 et versions ultérieures des systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-129">.NET Framework 3.5 is supported on Windows XP versions of Windows client operating systems, and on Windows Server 2003 and later versions of Windows server operating systems.</span></span>

    > [!Note]  
    > <span data-ttu-id="e3b9c-130">Nous recommandons l’utilisation de .NET Framework pour la création de documents XPS dans des applications clientes uniquement, et non dans des applications serveur, à moins que l’application ne se ferme régulièrement, comme c’est le cas pour une application cliente.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-130">We recommend the use of .NET Framework for creating XPS documents in client applications only, not in server applications unless the application exits periodically, as it would if it were a client application.</span></span>

     

    <span data-ttu-id="e3b9c-131">Pour plus d’informations sur la prise en charge des documents dans .NET Framework, consultez [Windows Presentation Foundation documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-131">For more information about document support in .NET Framework, see [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="e3b9c-132">Pour travailler avec des documents XPS dans un programme, utilisez l’API de document XPS native ou le .NET Framework. l’utilisation simultanée des deux dans le même programme n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-132">To work with XPS documents in a program, use either the native XPS Document API or the .NET Framework; simultaneous use of both in the same program is not supported.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="e3b9c-133">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e3b9c-133">In This Section</span></span>

<span data-ttu-id="e3b9c-134">Cette section décrit les technologies de document Windows natives prises en charge par Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-134">This section describes the native Windows document technologies that are supported by Microsoft Windows.</span></span>



|                                                                    |                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3b9c-135">API de document XPS</span><span class="sxs-lookup"><span data-stu-id="e3b9c-135">XPS Document API</span></span>](documents-xps.md)<br/>                   | <span data-ttu-id="e3b9c-136">Fournit un format fiable pour le papier électronique.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-136">Provides a trustworthy format for electronic paper.</span></span><br/> <span data-ttu-id="e3b9c-137">L’API de document XPS décrite dans cette section donne aux programmes et aux pilotes d’impression XPSDrv l’accès au contenu et aux métadonnées d’un document XPS.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-137">The XPS Document API that is described in this section gives programs and XPSDrv print drivers access to the content and metadata of an XPS document.</span></span><br/> |
| [<span data-ttu-id="e3b9c-138">API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="e3b9c-138">XPS Digital Signature API</span></span>](xps-digital-signatures.md)<br/> | <span data-ttu-id="e3b9c-139">Active la signature de documents, la vérification de l’identité du signataire et l’indication si un document XPS a été modifié depuis sa signature.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-139">Enables document signing, verification of the signer's identity, and indication of whether an XPS document has changed since it was signed.</span></span><br/>                                                                          |
| [<span data-ttu-id="e3b9c-140">Glossaire de documents XPS</span><span class="sxs-lookup"><span data-stu-id="e3b9c-140">XPS Documents Glossary</span></span>](xpsapi-glossary.md)<br/>           | <span data-ttu-id="e3b9c-141">Définitions des termes utilisés par l' [API de document XPS](documents-xps.md) et l' [API de signature numérique XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-141">Definitions of terms used by the [XPS Document API](documents-xps.md) and the [XPS Digital Signature API](xps-digital-signatures.md).</span></span><br/>                                                                              |



 

## <a name="xps-document-tools"></a><span data-ttu-id="e3b9c-142">Outils de document XPS</span><span class="sxs-lookup"><span data-stu-id="e3b9c-142">XPS Document Tools</span></span>

<span data-ttu-id="e3b9c-143">Les outils suivants sont disponibles pour vous aider à tester et à résoudre les problèmes liés aux fichiers de document XPS.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-143">The following tools are available to assist you with testing and troubleshooting of XPS document files.</span></span>

-   <span data-ttu-id="e3b9c-144">[IsXPS](/previous-versions/aa348104(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="e3b9c-144">[IsXPS](/previous-versions/aa348104(v=vs.110))</span></span>

    <span data-ttu-id="e3b9c-145">Teste la conformité d’un fichier aux spécifications XPS (XML Paper Specification) et OPC (Open Packaging Conventions).</span><span class="sxs-lookup"><span data-stu-id="e3b9c-145">Tests a file's conformity to the XML Paper Specification (XPS) and the Open Packaging Conventions (OPC) Specification.</span></span>

-   [<span data-ttu-id="e3b9c-146">XpsAnalyzer</span><span class="sxs-lookup"><span data-stu-id="e3b9c-146">XpsAnalyzer</span></span>](/windows-hardware/drivers/devtest/xpsanalyzer)

    <span data-ttu-id="e3b9c-147">Outil d’invite de commandes qui analyse les fichiers de document XPS pour la compatibilité avec la spécification XPS 1,0.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-147">A command-prompt tool that analyzes XPS document files for compatibility with the XPS 1.0 specification.</span></span>

-   <span data-ttu-id="e3b9c-148">[PTConform](/previous-versions/dd327476(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e3b9c-148">[PTConform](/previous-versions/dd327476(v=msdn.10))</span></span>

    <span data-ttu-id="e3b9c-149">Outil qui vérifie la validité des documents PrintTicket et PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="e3b9c-149">A tool that checks the validity of PrintTicket and PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3b9c-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3b9c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3b9c-151">API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="e3b9c-151">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[<span data-ttu-id="e3b9c-152">Packaging</span><span class="sxs-lookup"><span data-stu-id="e3b9c-152">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="e3b9c-153">Impression</span><span class="sxs-lookup"><span data-stu-id="e3b9c-153">Printing</span></span>](./printdocs-printing.md)
</dt> <dt>
  
<span data-ttu-id="e3b9c-154">[Imprimer un exemple de programme](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="e3b9c-154">[Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span></span>
</dt> </dl>

 

