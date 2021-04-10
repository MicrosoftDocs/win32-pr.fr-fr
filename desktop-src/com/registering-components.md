---
title: Inscription des composants
description: Inscription des composants
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031897"
---
# <a name="registering-components"></a><span data-ttu-id="68b0b-103">Inscription des composants</span><span class="sxs-lookup"><span data-stu-id="68b0b-103">Registering Components</span></span>

<span data-ttu-id="68b0b-104">Lorsque les types d’applications suivants sont installés, les informations d’installation doivent être ajoutées au registre, généralement par le biais d’un programme d’installation :</span><span class="sxs-lookup"><span data-stu-id="68b0b-104">When the following types of applications are installed, installation information must be added to the registry, usually through a setup program:</span></span>

-   <span data-ttu-id="68b0b-105">Applications serveur</span><span class="sxs-lookup"><span data-stu-id="68b0b-105">Server applications</span></span>
-   <span data-ttu-id="68b0b-106">Applications conteneur/serveur</span><span class="sxs-lookup"><span data-stu-id="68b0b-106">Container/server applications</span></span>
-   <span data-ttu-id="68b0b-107">Applications conteneur qui autorisent la liaison à des objets incorporés</span><span class="sxs-lookup"><span data-stu-id="68b0b-107">Container applications that allow linking to embedded objects</span></span>

<span data-ttu-id="68b0b-108">Pour les trois instances, inscrivez les informations de bibliothèque COM (DLL) et les informations spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="68b0b-108">For all three instances, register COM library (DLL) information and application-specific information.</span></span>

<span data-ttu-id="68b0b-109">La DLL enregistre les informations de tous ses composants en exportant [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="68b0b-109">The DLL registers the information for all its components by exporting [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="68b0b-110">Utilisez les fonctions suivantes pour inscrire et annuler l’inscription d’un composant :</span><span class="sxs-lookup"><span data-stu-id="68b0b-110">Use the following functions to register and unregister a component:</span></span>

-   [<span data-ttu-id="68b0b-111">**RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="68b0b-111">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [<span data-ttu-id="68b0b-112">**RegCreateKeyEx**</span><span class="sxs-lookup"><span data-stu-id="68b0b-112">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="68b0b-113">**RegSetValueEx**</span><span class="sxs-lookup"><span data-stu-id="68b0b-113">**RegSetValueEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [<span data-ttu-id="68b0b-114">**RegEnumKeyEx**</span><span class="sxs-lookup"><span data-stu-id="68b0b-114">**RegEnumKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [<span data-ttu-id="68b0b-115">**RegDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="68b0b-115">**RegDeleteKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [<span data-ttu-id="68b0b-116">**Échec RegCloseKey**</span><span class="sxs-lookup"><span data-stu-id="68b0b-116">**RegCloseKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a><span data-ttu-id="68b0b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68b0b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68b0b-118">Inscription des applications COM</span><span class="sxs-lookup"><span data-stu-id="68b0b-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 