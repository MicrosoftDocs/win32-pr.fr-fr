---
description: Wmiadap est une application qui s’exécute sur Windows et qui peut mettre à jour les informations de performances dans le référentiel WMI.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5d2de65e8566283b341c5af52048cc79cc0299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210720"
---
# <a name="wmiadap"></a><span data-ttu-id="ff1b4-103">wmiadap</span><span class="sxs-lookup"><span data-stu-id="ff1b4-103">wmiadap</span></span>

<span data-ttu-id="ff1b4-104">Wmiadap est une application qui s’exécute sur Windows et qui peut mettre à jour les informations de performances dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="ff1b4-104">Wmiadap is a application that runs on Windows that can update performance information in the WMI repository.</span></span> <span data-ttu-id="ff1b4-105">En général, cela permet aux développeurs et aux administrateurs informatiques de créer des scripts qui accèdent aux informations sur les performances, telles que la quantité de mémoire utilisée par une application.</span><span class="sxs-lookup"><span data-stu-id="ff1b4-105">Generally, this allows developers and IT Administrators to create scripts that access performance information, such as the amount of memory used by an application.</span></span> <span data-ttu-id="ff1b4-106">La rubrique suivante décrit l’interface de ligne de commande que vous pouvez utiliser pour contrôler la façon dont wmiadap récupère les informations.</span><span class="sxs-lookup"><span data-stu-id="ff1b4-106">The following topic describes the command-line interface you can use to control how wmiadap retrieves information.</span></span>

<span data-ttu-id="ff1b4-107">Wmiadap est installé avec le système d’exploitation sur la plupart des systèmes, dans le répertoire C : \\ Windows \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="ff1b4-107">Wmiadap is installed with the operating system on most systems, in the C:\\Windows\\System32\\wbem directory.</span></span> <span data-ttu-id="ff1b4-108">Si vous constatez des messages d’erreur concernant wmiadap.exe, recherchez [support Microsoft](https://support.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ff1b4-108">If you are seeing error messages concerning wmiadap.exe, search [Microsoft Support](https://support.microsoft.com/).</span></span> <span data-ttu-id="ff1b4-109">En règle générale, vous ne devez pas supprimer wmiadap.exe de votre système, sauf instruction contraire.</span><span class="sxs-lookup"><span data-stu-id="ff1b4-109">Generally, you should not delete wmiadap.exe from your system, unless otherwise instructed.</span></span>

<span data-ttu-id="ff1b4-110">Le transfert de données à partir des bibliothèques de performance et l’actualisation des classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) sont effectués par les fournisseurs [WmiPerfClass](wmi-providers.md) et [wmiperfinst](wmi-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="ff1b4-110">The transfer of data from the performance libraries and the refresh of classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) is done by the [WmiPerfClass](wmi-providers.md) and [WMIPerfInst](wmi-providers.md) providers.</span></span> <span data-ttu-id="ff1b4-111">Le fournisseur WmiPerfClass met à jour les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI uniquement lorsqu’un nouvel objet de performance est ajouté.</span><span class="sxs-lookup"><span data-stu-id="ff1b4-111">The WmiPerfClass provider updates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) only when a new performance object is added.</span></span> <span data-ttu-id="ff1b4-112">Vous pouvez toujours exécuter wmiadap avec le commutateur **/r** pour analyser les pilotes Windows Driver Model afin de créer des objets de performance.</span><span class="sxs-lookup"><span data-stu-id="ff1b4-112">You still can run Wmiadap with the **/r** switch to parse the Windows Driver Model drivers to create performance objects.</span></span> <span data-ttu-id="ff1b4-113">Le commutateur **/f** force toujours une mise à jour des classes WMI à partir des bibliothèques de performances.</span><span class="sxs-lookup"><span data-stu-id="ff1b4-113">The **/f** switch still forces an update of the WMI classes from the performance libraries.</span></span>

<span data-ttu-id="ff1b4-114">Les commutateurs suivants sont disponibles à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="ff1b4-114">The following switches are available at the command prompt.</span></span>

<span data-ttu-id="ff1b4-115">**wmiadap** \[  \] /f \[ **/r**\]</span><span class="sxs-lookup"><span data-stu-id="ff1b4-115">**wmiadap** \[**/f**\]\[**/r**\]</span></span>

## <a name="switches"></a><span data-ttu-id="ff1b4-116">Commutateurs</span><span class="sxs-lookup"><span data-stu-id="ff1b4-116">Switches</span></span>

<dl> <dt>

<span data-ttu-id="ff1b4-117"><span id="_f"></span><span id="_F"></span>**/f**</span><span class="sxs-lookup"><span data-stu-id="ff1b4-117"><span id="_f"></span><span id="_F"></span>**/f**</span></span>
</dt> <dd>

<span data-ttu-id="ff1b4-118">Analyse toutes les bibliothèques de performances du système et actualise les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="ff1b4-118">Parses all the performance libraries on the system and refreshes the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

</dd> <dt>

<span data-ttu-id="ff1b4-119"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="ff1b4-119"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="ff1b4-120">Analyse tous les pilotes Windows Driver Model sur le système pour créer des objets de performance.</span><span class="sxs-lookup"><span data-stu-id="ff1b4-120">Parses all the Windows Driver Model drivers on the system to create performance objects.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="ff1b4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff1b4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff1b4-122">Bibliothèques de performances et WMI</span><span class="sxs-lookup"><span data-stu-id="ff1b4-122">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="ff1b4-123">**critique**</span><span class="sxs-lookup"><span data-stu-id="ff1b4-123">**winmgmt**</span></span>](winmgmt.md)
</dt> </dl>

 

 
