---
description: L’une des façons de créer des applications Web avec accès manuscrit consiste à placer des contrôles de Windows Forms dans awebpagewithin Microsoft Internet Explorer.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Contrôles Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b28fa2a3293b6b780412ddbc755634c745b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515642"
---
# <a name="web-controls"></a><span data-ttu-id="a3bec-103">Contrôles Web</span><span class="sxs-lookup"><span data-stu-id="a3bec-103">Web Controls</span></span>

<span data-ttu-id="a3bec-104">L’une des façons de créer des applications Web avec accès manuscrit consiste à placer des contrôles de Windows Forms dans awebpagewithin Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a3bec-104">One way to create ink-enabled Web applications is to put Windows Forms controls inside awebpagewithin Microsoft Internet Explorer.</span></span> <span data-ttu-id="a3bec-105">Un bon didacticiel sur cette technique est disponible à [l’aide des contrôles de Windows Forms dans Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span><span class="sxs-lookup"><span data-stu-id="a3bec-105">A good tutorial on this technique can be found at [Using Windows Forms Controls in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span></span> <span data-ttu-id="a3bec-106">Les étapes de base du didacticiel sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3bec-106">The basic steps in the tutorial are:</span></span>

1.  <span data-ttu-id="a3bec-107">Créez un contrôle qui hérite de [**System. Windows. Forms. UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="a3bec-107">Create a control that inherits from [**System.Windows.Forms.UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).</span></span>
2.  <span data-ttu-id="a3bec-108">Créez une page HTML avec une balise d’objet qui fait référence à ce UserControl.</span><span class="sxs-lookup"><span data-stu-id="a3bec-108">Create an HTML page with an object tag that refers to that UserControl.</span></span>
3.  <span data-ttu-id="a3bec-109">Créez un répertoire virtuel et définissez des autorisations.</span><span class="sxs-lookup"><span data-stu-id="a3bec-109">Create a virtual directory and set permissions.</span></span>
4.  <span data-ttu-id="a3bec-110">Chargez l’URL de la page HTML dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="a3bec-110">Load the URL of the HTML page into the browser.</span></span>

<span data-ttu-id="a3bec-111">Cette technique peut être appliquée à des contrôles compatibles avec l’encre, comme n’importe quel autre [**contrôle**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)de Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="a3bec-111">This technique can be applied to ink-enabled controls, just like any other Windows Forms [**Control**](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="a3bec-112">En fait, la technique peut être utilisée avec n’importe quelle classe de l’infrastructure Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="a3bec-112">In fact, the technique can be used with any class in the Microsoft .NET Framework.</span></span> <span data-ttu-id="a3bec-113">Les exemples fournis par le kit de développement logiciel (SDK) de Microsoft Windows XP Tablet PC Edition incluent une version de contrôle Web de l’exemple de revendications automatiques dans la section des exemples Web Ink.</span><span class="sxs-lookup"><span data-stu-id="a3bec-113">The samples provided by the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) include a Web control version of the Auto Claims sample in the Ink Web Samples section.</span></span> <span data-ttu-id="a3bec-114">Cet exemple prend l' [exemple de formulaire de déclaration automatique](auto-claims-form-sample.md) d’origine et le transforme en un contrôle qui est placé sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="a3bec-114">This example takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span> <span data-ttu-id="a3bec-115">Pour plus d’informations sur l’activation de cet exemple sur le Web, consultez l ['exemple de contrôle Web Ink](ink-web-control-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a3bec-115">For more information about Web-enabling this sample, see the [Ink Web Control Sample](ink-web-control-sample.md).</span></span>

> [!Note]  
> <span data-ttu-id="a3bec-116">Lorsque vous déployez une application créée à l’aide de .NET sur le Web, l’application peut être affectée par le modèle de sécurité pour .NET.</span><span class="sxs-lookup"><span data-stu-id="a3bec-116">When you deploy an application created by using .NET over the Web, the application may be affected by security model for .NET.</span></span> <span data-ttu-id="a3bec-117">Pour plus d’informations sur le fonctionnement de la sécurité avec les applications Web prenant en charge l’écriture manuscrite, consultez [sécurité et confiance](security-and-trust.md).</span><span class="sxs-lookup"><span data-stu-id="a3bec-117">For more information about how security works with ink-enabled Web applications, see [Security and Trust](security-and-trust.md).</span></span>

 

 

 
