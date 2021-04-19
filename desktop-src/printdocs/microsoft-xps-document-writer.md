---
description: Microsoft XPS document Writer (MXDW) est un pilote d’impression à fichier qui permet à une application Windows de créer des fichiers de document XPS (XML Paper Specification) sur des versions de Windows à partir de Windows XP avec Service Pack 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Microsoft XPS document Writer (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520770"
---
# <a name="microsoft-xps-document-writer-mxdw"></a><span data-ttu-id="e17a6-103">Microsoft XPS document Writer (MXDW)</span><span class="sxs-lookup"><span data-stu-id="e17a6-103">Microsoft XPS Document Writer (MXDW)</span></span>

<span data-ttu-id="e17a6-104">Microsoft XPS document Writer (MXDW) est un pilote d’impression à fichier qui permet à une application Windows de créer des fichiers de document XPS (XML Paper Specification) sur des versions de Windows à partir de Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="e17a6-104">The Microsoft XPS Document Writer (MXDW) is a print-to-file driver that enables a Windows application to create XML Paper Specification (XPS) document files on versions of Windows starting with Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="e17a6-105">L’utilisation de MXDW permet à une application Windows d’enregistrer son contenu en tant que document XPS sans modifier le code de programme de l’application.</span><span class="sxs-lookup"><span data-stu-id="e17a6-105">Using the MXDW makes it possible for a Windows application to save its content as an XPS document without changing any of the application's program code.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e17a6-106">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="e17a6-106">When to Use</span></span>

<span data-ttu-id="e17a6-107">En tant qu’utilisateur, vous devez sélectionner le MXDW lorsque vous souhaitez créer un document XPS à partir d’une application Windows qui n’a pas la possibilité d’enregistrer son contenu en tant que document XPS.</span><span class="sxs-lookup"><span data-stu-id="e17a6-107">As a user, you would select the MXDW when you want to create an XPS document from a Windows application that does not have the option to save its content as an XPS document.</span></span>

<span data-ttu-id="e17a6-108">En tant que développeur d’applications, vous recommandez le MXDW aux utilisateurs qui souhaitent créer des documents XPS lorsque votre application n’offre pas la possibilité d’enregistrer en tant que document XPS.</span><span class="sxs-lookup"><span data-stu-id="e17a6-108">As an application developer, you would recommend the MXDW to users who want to create XPS documents when your application does not offer the option to save as an XPS document.</span></span> <span data-ttu-id="e17a6-109">Pour plus d’informations sur la spécification XML Paper et les documents XPS, consultez [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) et [XPS Specification et License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)(en anglais).</span><span class="sxs-lookup"><span data-stu-id="e17a6-109">For more information on the XML Paper Specification and XPS documents, see [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) and [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

<span data-ttu-id="e17a6-110">Le MXDW est installé automatiquement sur Windows Vista et les versions ultérieures de Windows et peut être téléchargé et installé sur Windows XP avec SP2 et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e17a6-110">The MXDW is installed automatically on Windows Vista and later versions of Windows and can be downloaded and installed on Windows XP with SP2 and Windows Server 2003.</span></span>

## <a name="installation"></a><span data-ttu-id="e17a6-111">Installation</span><span class="sxs-lookup"><span data-stu-id="e17a6-111">Installation</span></span>

<span data-ttu-id="e17a6-112">Sur Windows Vista et les versions ultérieures de Windows, le MXDW est installé automatiquement lors de l’installation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e17a6-112">On Windows Vista and later versions of Windows, the MXDW is installed automatically when the operating system is installed.</span></span>

<span data-ttu-id="e17a6-113">**Windows XP avec SP2 et Windows Server 2003**: téléchargez et installez .net Framework 3,0 ou XPS Essential Pack à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/en/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="e17a6-113">**Windows XP with SP2 and Windows Server 2003**: Download and install either .Net Framework 3.0 or the XPS Essential Pack from the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx).</span></span>

## <a name="how-to-use"></a><span data-ttu-id="e17a6-114">Utilisation</span><span class="sxs-lookup"><span data-stu-id="e17a6-114">How to Use</span></span>

<span data-ttu-id="e17a6-115">Une fois installé, le MXDW apparaît comme une file d’attente à l’impression disponible dans la boîte de dialogue Imprimer présentée par une application.</span><span class="sxs-lookup"><span data-stu-id="e17a6-115">When installed, the MXDW appears as an available print queue in the Print dialog box presented by an application.</span></span> <span data-ttu-id="e17a6-116">Lorsque le MXDW est sélectionné comme imprimante, l’utilisateur est invité à entrer le nom de fichier à créer comme document XPS qui capture la sortie d’impression de l’application.</span><span class="sxs-lookup"><span data-stu-id="e17a6-116">When the MXDW is selected as the printer, the user is prompted for the file name to create as the XPS Document that captures the print output of the application.</span></span>

<span data-ttu-id="e17a6-117">L’illustration suivante montre le MXDW sélectionné comme imprimante dans la boîte de dialogue d’impression commune de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e17a6-117">The following image shows the MXDW being selected as the printer in the Windows Vista common print dialog box.</span></span>

![image de la boîte de dialogue Imprimer qui affiche la sélection de Microsoft XPS document Writer (MXDW)](images/choosingmxdwinvista.gif)

<span data-ttu-id="e17a6-119">Les développeurs d’applications peuvent personnaliser la sortie de MXDW à l’aide des [paramètres de configuration MXDW](mxdw-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e17a6-119">Application developers can customize the output of MXDW using the [MXDW configuration settings](mxdw-configuration-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e17a6-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e17a6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e17a6-121">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="e17a6-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="e17a6-122">Spécifications XPS et téléchargements de licences</span><span class="sxs-lookup"><span data-stu-id="e17a6-122">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

<span data-ttu-id="e17a6-123">[Outil de conformité isXPS](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e17a6-123">[isXPS Conformance Tool](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e17a6-124">Paramètres de configuration de MXDW</span><span class="sxs-lookup"><span data-stu-id="e17a6-124">MXDW configuration settings</span></span>](mxdw-configuration-settings.md)
</dt> </dl>

 

 
