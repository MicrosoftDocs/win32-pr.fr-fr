---
title: Fournir des autorisations utilisateur pour les appareils de gravure de médias
description: Par défaut, Windows Vista et Windows Server 2008 accordent un accès en lecture/écriture aux administrateurs et aux utilisateurs connectés directement à l’ordinateur (utilisateurs intermédiaires).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104211167"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a><span data-ttu-id="7cda9-103">Fournir des autorisations utilisateur pour les appareils de gravure de médias</span><span class="sxs-lookup"><span data-stu-id="7cda9-103">Providing User Permissions for Media Burning Devices</span></span>

<span data-ttu-id="7cda9-104">Par défaut, Windows Vista et Windows Server 2008 accordent un accès en lecture/écriture aux administrateurs et aux utilisateurs connectés directement à l’ordinateur (utilisateurs intermédiaires).</span><span class="sxs-lookup"><span data-stu-id="7cda9-104">By default, both Windows Vista and Windows Server 2008 grant read/write access to administrators and users logged directly into the machine (intermediate users).</span></span> <span data-ttu-id="7cda9-105">Toutefois, dans Windows XP et Windows Server 2003, un administrateur doit accorder ces privilèges de lecture/écriture à d’autres groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7cda9-105">However, in Windows XP and Windows Server 2003 an administrator must grant these device read/write privileges to other user groups.</span></span>

<span data-ttu-id="7cda9-106">Un administrateur peut ajuster des autorisations spécifiques à un appareil pour les utilisateurs avec pouvoir et les utilisateurs interactifs.</span><span class="sxs-lookup"><span data-stu-id="7cda9-106">An administrator may adjust specific device-related permissions for power users and interactive users.</span></span>

<span data-ttu-id="7cda9-107">Pour accéder au panneau autorisations appropriées du groupe dans Windows XP, cliquez sur **Démarrer**, sur **exécuter**, tapez **gpedit. msc**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cda9-107">To reach the appropriate group permissions panel in Windows XP, click **Start**, click **Run**, type **gpedit.msc**, and then click **OK**.</span></span> <span data-ttu-id="7cda9-108">Dans l’interface stratégie de groupe, développez successivement **Configuration ordinateur**, **Paramètres Windows**, **paramètres de sécurité**, **stratégies locales**, puis double-cliquez sur **options de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="7cda9-108">In the Group Policy interface, expand **Computer Configuration**, expand **Windows Settings**, expand **Security Settings**, expand **Local Policies**, and double-click **Security Options**.</span></span>

![Capture d’écran montrant la fenêtre « stratégie de groupe » avec une stratégie sélectionnée à partir du volet « stratégie ».](images/gpolpanel.jpg)

<span data-ttu-id="7cda9-110">Dans ce panneau, un administrateur doit spécifier les paramètres de deux options d’appareil pour fournir les autorisations de groupe requises :</span><span class="sxs-lookup"><span data-stu-id="7cda9-110">At this panel, an administrator must specify the settings of two device options to provide the required group permissions:</span></span>

-   <span data-ttu-id="7cda9-111">Définir « appareils : restreindre l’accès à un CD-ROM à un utilisateur connecté localement » à **activé**</span><span class="sxs-lookup"><span data-stu-id="7cda9-111">Set "Devices: Restrict CD-ROM access to locally logged-on user only" to **Enabled**</span></span>
-   <span data-ttu-id="7cda9-112">Définissez « appareils : autorisés à formater et éjecter les supports amovibles » pour **les administrateurs et les utilisateurs avec pouvoir**.</span><span class="sxs-lookup"><span data-stu-id="7cda9-112">Set "Devices: Allowed to format and eject removable media" to **Administrators and Power Users**.</span></span> <span data-ttu-id="7cda9-113">Il est également possible d’émuler les autorisations Windows Vista en définissant cette option sur **administrateurs et utilisateurs interactifs**.</span><span class="sxs-lookup"><span data-stu-id="7cda9-113">It is also possible to emulate Windows Vista permissions by setting this option to **Administrators and Interactive Users**.</span></span>

<span data-ttu-id="7cda9-114">Bien qu’une interface utilisateur spécifique n’existe pas dans Windows XP ou Windows Server 2003 pour l’utilisation de [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) ou [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), il est possible d’utiliser ces API pour accorder des autorisations d’appareil aux groupes d’utilisateurs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="7cda9-114">While a specific UI does not exist in Windows XP or Windows Server 2003 for the use of [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) or [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), it is possible to use these APIs to grant custom user groups device permissions.</span></span> <span data-ttu-id="7cda9-115">Par exemple, un appel à **SetSecurityInfo** accorde des autorisations à des groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7cda9-115">For example, a call to **SetSecurityInfo** will grant permissions to user groups.</span></span> <span data-ttu-id="7cda9-116">Les modifications apportées aux autorisations avec cette API sont temporaires et ne sont pas conservées au redémarrage.</span><span class="sxs-lookup"><span data-stu-id="7cda9-116">Permission changes with this API are temporary and will not persist across a reboot.</span></span> <span data-ttu-id="7cda9-117">Toutefois, l’appel de [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) implémente les modifications d’autorisation dans le registre, qui sont conservées au cours d’un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="7cda9-117">However, calling [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) will implement the permission changes in the registry, which will persist across a reboot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cda9-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7cda9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cda9-119">Utilisation d’IMAPi</span><span class="sxs-lookup"><span data-stu-id="7cda9-119">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="7cda9-120">**SetSecurityInfo**</span><span class="sxs-lookup"><span data-stu-id="7cda9-120">**SetSecurityInfo**</span></span>](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[<span data-ttu-id="7cda9-121">SetupDiSetDeviceRegistryProperty</span><span class="sxs-lookup"><span data-stu-id="7cda9-121">SetupDiSetDeviceRegistryProperty</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 