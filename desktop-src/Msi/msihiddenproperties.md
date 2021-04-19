---
description: La propriété MsiHiddenProperties peut être utilisée pour empêcher le programme d’installation d’afficher des mots de passe ou d’autres informations confidentielles dans le fichier journal.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Propriété MsiHiddenProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530560"
---
# <a name="msihiddenproperties-property"></a><span data-ttu-id="9ba3b-103">Propriété MsiHiddenProperties</span><span class="sxs-lookup"><span data-stu-id="9ba3b-103">MsiHiddenProperties property</span></span>

<span data-ttu-id="9ba3b-104">La propriété **MsiHiddenProperties** peut être utilisée pour empêcher le programme d’installation d’afficher des mots de passe ou d’autres informations confidentielles dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-104">The **MsiHiddenProperties** property may be used to prevent the installer from displaying passwords or other confidential information in the log file.</span></span> <span data-ttu-id="9ba3b-105">Pour empêcher une propriété d’être écrite dans le fichier journal, définissez la valeur de la propriété **MsiHiddenProperties** sur le nom de la propriété que vous souhaitez masquer.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-105">To prevent a property from being written into the log file, set the value of the **MsiHiddenProperties** property to the name of the property you wish to hide.</span></span> <span data-ttu-id="9ba3b-106">Vous pouvez masquer plusieurs propriétés en spécifiant une chaîne de noms de propriétés délimitée par des points-virgules (;).</span><span class="sxs-lookup"><span data-stu-id="9ba3b-106">You can hide multiple properties by specifying a string of property names delimited by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="9ba3b-107">Lorsque la stratégie de [débogage](debug.md) est définie sur 7, le programme d’installation écrit les informations entrées sur une ligne de commande dans le journal.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-107">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="9ba3b-108">Cela rend les propriétés publiques entrées sur une ligne de commande visibles, même si la propriété est incluse dans la propriété **MsiHiddenProperties** .</span><span class="sxs-lookup"><span data-stu-id="9ba3b-108">This makes public properties entered on a command line visible even if the property is included in the **MsiHiddenProperties** property.</span></span> <span data-ttu-id="9ba3b-109">Cela peut rendre les informations confidentielles entrées sur une ligne de commande visible dans le journal.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-109">This can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="9ba3b-110">Pour plus d’informations, consultez [la page empêcher l’écriture d’informations confidentielles dans le fichier journal](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="9ba3b-110">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ba3b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ba3b-111">Requirements</span></span>



| <span data-ttu-id="9ba3b-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ba3b-112">Requirement</span></span> | <span data-ttu-id="9ba3b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ba3b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba3b-114">Version</span><span class="sxs-lookup"><span data-stu-id="9ba3b-114">Version</span></span><br/> | <span data-ttu-id="9ba3b-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9ba3b-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9ba3b-117">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9ba3b-118">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9ba3b-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ba3b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ba3b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba3b-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9ba3b-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




