---
description: Le Windows Installer prend en charge la publication d’applications et de fonctionnalités.
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: Prise en charge des plateformes de la publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523114"
---
# <a name="platform-support-of-advertisement"></a><span data-ttu-id="28dff-103">Prise en charge des plateformes de la publication</span><span class="sxs-lookup"><span data-stu-id="28dff-103">Platform Support of Advertisement</span></span>

<span data-ttu-id="28dff-104">Le Windows Installer prend en charge la publication d’applications et de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="28dff-104">The Windows Installer supports advertisement of applications and features.</span></span>

<span data-ttu-id="28dff-105">Les fonctionnalités de publication suivantes sont disponibles sur Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="28dff-105">The following advertisement capabilities are available on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP, and Windows 2000.</span></span>

-   <span data-ttu-id="28dff-106">Raccourcis et leurs icônes.</span><span class="sxs-lookup"><span data-stu-id="28dff-106">Shortcuts and their icons.</span></span>

-   <span data-ttu-id="28dff-107">Extensions et leurs icônes spécifiées dans la [table ProgID](progid-table.md).</span><span class="sxs-lookup"><span data-stu-id="28dff-107">Extensions and their icons specified in the [ProgId Table](progid-table.md).</span></span>

-   <span data-ttu-id="28dff-108">Verbes de Shell et de commande inscrits sous la clé ProgId.</span><span class="sxs-lookup"><span data-stu-id="28dff-108">Shell and command Verbs registered underneath the ProgId key.</span></span>

-   <span data-ttu-id="28dff-109">Contextes CLSID et InProcHandler.</span><span class="sxs-lookup"><span data-stu-id="28dff-109">CLSID contexts and InProcHandler.</span></span>

-   <span data-ttu-id="28dff-110">L’installation à la demande via OLE est disponible uniquement par programmation via [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++) et la **fonction CreateObject (Visual Basic)** ou la **fonction GetObject (Visual Basic)**.</span><span class="sxs-lookup"><span data-stu-id="28dff-110">Install-On-Demand through OLE is only available programmatically through [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++), and **CreateObject Function (Visual Basic)** or **GetObject Function (Visual Basic)**.</span></span>

> [!Note]
> <span data-ttu-id="28dff-111">Les informations AppId et TypeLib sont écrites uniquement lorsqu’un composant publié est installé.</span><span class="sxs-lookup"><span data-stu-id="28dff-111">AppId and Typelib information is only written when an advertised component is installed.</span></span>
> 
> <span data-ttu-id="28dff-112">Pour prendre en charge les extensions de nom de fichier, l’application doit être publiée sur Active Directory par un administrateur à l’aide de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="28dff-112">To support file name extensions, the application must be published to Active Directory by an administrator using Group Policy.</span></span>

## <a name="remarks"></a><span data-ttu-id="28dff-113">Notes</span><span class="sxs-lookup"><span data-stu-id="28dff-113">Remarks</span></span>

<span data-ttu-id="28dff-114">L’installation du produit peut ne pas nécessiter un redémarrage, mais tous les raccourcis publiés ne fonctionnent pas tant que l’ordinateur n’est pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="28dff-114">The installation of the product may not require a restart, but any advertised shortcuts do not work until the machine is restarted.</span></span> <span data-ttu-id="28dff-115">Les raccourcis publiés des installations suivantes fonctionnent sans redémarrage.</span><span class="sxs-lookup"><span data-stu-id="28dff-115">The advertised shortcuts of subsequent installations work without a restart.</span></span>

<span data-ttu-id="28dff-116">Pour garantir le bon fonctionnement des raccourcis publiés, l’auteur du package doit planifier un redémarrage forcé à la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="28dff-116">To ensure that advertised shortcuts work correctly, the package author should schedule a forced restart at the end of the installation.</span></span>

<span data-ttu-id="28dff-117">Pour éviter les redémarrages inutiles du système, planifiez un redémarrage pour qu’il s’exécute uniquement si aucune version du Windows Installer n’est installée.</span><span class="sxs-lookup"><span data-stu-id="28dff-117">To avoid unnecessary restarts of the system, schedule a restart to run only if no version of the Windows Installer is installed.</span></span>

<span data-ttu-id="28dff-118">Les instructions conditionnelles peuvent vérifier la propriété [**ShellAdvtSupport**](shelladvtsupport.md) et la propriété [**Version9X**](version9x.md) .</span><span class="sxs-lookup"><span data-stu-id="28dff-118">Conditional statements can check the [**ShellAdvtSupport**](shelladvtsupport.md) property and [**Version9X**](version9x.md) property.</span></span> <span data-ttu-id="28dff-119">Pour plus d’informations sur la planification d’un redémarrage forcé conditionnel, consultez [redémarrages système](system-reboots.md) et [utilisation de propriétés dans des instructions conditionnelles](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="28dff-119">For more information about scheduling a conditional forced restarts, see [System Reboots](system-reboots.md) and [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

 

 
