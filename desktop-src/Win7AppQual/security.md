---
description: Sécurité (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sécurité (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f320f4cb561079380e19a969eba95f3f6b321fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116227"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="81a74-103">Sécurité (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)</span><span class="sxs-lookup"><span data-stu-id="81a74-103">Security (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="81a74-104">À compter de Windows Internet Explorer 7, Windows Internet Explorer s’exécute dans un contexte de sécurité appelé *mode protégé* quand les utilisateurs l’exécutent sur le système d’exploitation Windows Vista ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="81a74-104">Starting with Windows Internet Explorer 7, Windows Internet Explorer runs in a security context called *Protected Mode* when users run it on the Windows Vista operating system or a later version.</span></span> <span data-ttu-id="81a74-105">Ce mode exécute Internet Explorer dans un paramètre de privilège inférieur à celui d’une application utilisateur standard, de sorte que certaines fonctionnalités sont limitées, en particulier les contrôles ActiveX et certains types de plug-ins. Pour plus d’informations sur le mode protégé dans Internet Explorer et son impact sur la compatibilité, consultez [présentation et utilisation en mode protégé d’Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) dans la bibliothèque MSDN.</span><span class="sxs-lookup"><span data-stu-id="81a74-105">This mode runs Internet Explorer in a lower-privilege setting than a standard user application so certain functionality is limited, especially ActiveX controls and certain types of plug-ins. For more information about Protected Mode in Internet Explorer and its impact on compatibility, see [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in the MSDN Library.</span></span>

<span data-ttu-id="81a74-106">Par défaut, Windows Internet Explorer 8 active également la prévention de l’exécution des données (DEP), qui permet aux applications d’éviter d’exécuter du code arbitraire dans les attaques en ligne.</span><span class="sxs-lookup"><span data-stu-id="81a74-106">By default, Windows Internet Explorer 8 also enables Data Execution Prevention (DEP), which helps applications avoid running arbitrary code in online attacks.</span></span> <span data-ttu-id="81a74-107">Toutefois, certains modules complémentaires peuvent ne pas utiliser cette fonctionnalité de sécurité (par exemple, tous les modules complémentaires qui ne sont pas conçus pour exécuter uniquement le code qui se trouve dans la mémoire qui a été spécifiquement marquée comme exécutable, comme les applications générées à l’aide d’une version antérieure de l’infrastructure ATL (ActiveX Template Library)).</span><span class="sxs-lookup"><span data-stu-id="81a74-107">However, some add-ons might not use this security feature (for example, any add-ons that are not designed to run only code that is located in memory that has been specifically marked as executable, such as applications that are built by using an older version of the ActiveX Template Library (ATL) framework).</span></span>

<span data-ttu-id="81a74-108">Internet Explorer 8 protège également les utilisateurs contre les failles de sécurité potentielles qui utilisent des scripts.</span><span class="sxs-lookup"><span data-stu-id="81a74-108">Internet Explorer 8 also protects users against potential security vulnerabilities that use scripts.</span></span> <span data-ttu-id="81a74-109">Par exemple, vous ne pouvez pas naviguer d’une URL dans une zone moins fiable vers une URL dans une zone plus fiable, sauf via une interaction utilisateur explicite.</span><span class="sxs-lookup"><span data-stu-id="81a74-109">For example, you cannot navigate from a URL in a less trusted zone to a URL in a more trusted zone except through explicit user interaction.</span></span> <span data-ttu-id="81a74-110">Vous ne pouvez pas non plus masquer certains éléments de l’interface utilisateur du navigateur (tels que la barre d’adresses) dans une zone non approuvée (Internet).</span><span class="sxs-lookup"><span data-stu-id="81a74-110">You also cannot hide certain elements of the browser’s user interface (such as the address bar) in an un-trusted (Internet) zone.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81a74-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81a74-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81a74-112">Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs</span><span class="sxs-lookup"><span data-stu-id="81a74-112">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
