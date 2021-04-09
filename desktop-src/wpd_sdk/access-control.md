---
description: Contrôle d’accès
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Access Control (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868273"
---
# <a name="access-control-wpd-api"></a><span data-ttu-id="a6aab-103">Access Control (API WPD)</span><span class="sxs-lookup"><span data-stu-id="a6aab-103">Access Control (WPD API)</span></span>

<span data-ttu-id="a6aab-104">Le Windows Driver Model (WDM) prend en charge la restriction de l’accès des appareils via les listes de Access Control (ACL) sur les nœuds de l’appareil Plug-and-Play (PnP).</span><span class="sxs-lookup"><span data-stu-id="a6aab-104">The Windows Driver Model (WDM) supports restricting device access via Access Control Lists (ACLs) on the Plug and Play (PnP) Device Nodes.</span></span> <span data-ttu-id="a6aab-105">Cela signifie que les fournisseurs et les administrateurs réseau peuvent restreindre l’accès à n’importe quel type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="a6aab-105">This means that vendors and network administrators can restrict access to any device type.</span></span> <span data-ttu-id="a6aab-106">Lorsqu’une application ouvre un handle à un pilote en appelant [**IPortableDevice :: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), le gestionnaire d’e/s du pilote vérifie si l’utilisateur donné dispose de l’accès requis, et effectue de la même manière des contrôles d’accès lorsque les IOCTL sont envoyées au pilote à partir de ce handle.</span><span class="sxs-lookup"><span data-stu-id="a6aab-106">When an application opens a handle to a driver by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), the driver's I/O Manager verifies whether the given user has the required access, and similarly does access checks when IOCTLs are sent to the driver from that handle.</span></span>

<span data-ttu-id="a6aab-107">Par exemple, un administrateur réseau peut restreindre les utilisateurs invités à l’accès en lecture seule pour les périphériques portables, alors qu’ils peuvent accorder aux utilisateurs authentifiés un accès en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a6aab-107">For example, a network administrator could restrict Guest users to read-only access for portable devices, while they could grant Authenticated users read/write access.</span></span> <span data-ttu-id="a6aab-108">Dans ce cas, cela implique que si un invité a émis une commande WPD nécessitant un accès en lecture/écriture (par exemple, supprimer un objet); elle échoue avec l’accès refusé, tandis que si un utilisateur authentifié a émis la même commande, elle réussit.</span><span class="sxs-lookup"><span data-stu-id="a6aab-108">In this case, it implies that if a Guest issued a WPD command that required read/write access (such as Delete Object); it would fail with Access Denied, whereas if an Authenticated user issued the same command, it would succeed.</span></span>

<span data-ttu-id="a6aab-109">Les entrées de stratégie de groupe pour le contrôle de l’accès au stockage amovible et aux périphériques portables ne sont en fait rien de plus qu’un moyen simple pour les administrateurs d’appliquer des ACL de nœuds de périphérique PnP à une classe entière d’appareils à la fois (par exemple, en appliquant l’autorisation « refuser l’accès en écriture aux périphériques portables stratégie de groupe ».</span><span class="sxs-lookup"><span data-stu-id="a6aab-109">The Group Policy entries for controlling access to removable storage and portable devices is actually nothing more than an easy way for Administrators to apply PnP device node ACLs to a whole class of devices at a time (for example, applying the "Deny Write Access to Portable Devices" Group Policy would adjust the ACLs of all WPD devices to deny write access).</span></span>

## <a name="io-control-codes-in-wpd"></a><span data-ttu-id="a6aab-110">Codes de contrôle d’e/s dans WPD</span><span class="sxs-lookup"><span data-stu-id="a6aab-110">I/O Control Codes in WPD</span></span>

<span data-ttu-id="a6aab-111">Les applications WPD communiquent avec les pilotes en ouvrant des descripteurs d’appareil et en envoyant des codes de contrôle d’e/s (IOCTL).</span><span class="sxs-lookup"><span data-stu-id="a6aab-111">WPD applications communicate with drivers by opening device handles and sending I/O Control Codes (IOCTLs).</span></span> <span data-ttu-id="a6aab-112">Ces IOCTL se composent de quatre sections :</span><span class="sxs-lookup"><span data-stu-id="a6aab-112">These IOCTLs consist of four sections:</span></span>

1.  <span data-ttu-id="a6aab-113">Type d’appareil</span><span class="sxs-lookup"><span data-stu-id="a6aab-113">Device Type</span></span>
2.  <span data-ttu-id="a6aab-114">Code de fonction</span><span class="sxs-lookup"><span data-stu-id="a6aab-114">Function Code</span></span>
3.  <span data-ttu-id="a6aab-115">Buffer, méthode</span><span class="sxs-lookup"><span data-stu-id="a6aab-115">Buffer Method</span></span>
4.  <span data-ttu-id="a6aab-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a6aab-116">Access Type</span></span>

<span data-ttu-id="a6aab-117">La quatrième section, le type d’accès, spécifie la spécification d’accès spécifique pour la commande donnée.</span><span class="sxs-lookup"><span data-stu-id="a6aab-117">The fourth section, the Access Type, specifies the specific access requirement for the given command.</span></span> <span data-ttu-id="a6aab-118">Le gestionnaire d’e/s du pilote utilise ces données pour effectuer la vérification de la liste de Access Control (ACL).</span><span class="sxs-lookup"><span data-stu-id="a6aab-118">The driver's I/O manager uses this data to perform the Access Control List (ACL) check.</span></span>

<span data-ttu-id="a6aab-119">Par conséquent, si une IOCTL a été définie comme :</span><span class="sxs-lookup"><span data-stu-id="a6aab-119">So if an IOCTL were defined as:</span></span>


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



<span data-ttu-id="a6aab-120">Le gestionnaire d’e/s du pilote vérifie que le propriétaire du descripteur de l’appareil dispose d’un accès en lecture à l’appareil lorsque ce message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="a6aab-120">The driver's I/O manager would check that the owner of the device handle has read access to the device when this message is sent.</span></span>

<span data-ttu-id="a6aab-121">Et, si une IOCTL a été définie comme :</span><span class="sxs-lookup"><span data-stu-id="a6aab-121">And, if an IOCTL were defined as:</span></span>


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



<span data-ttu-id="a6aab-122">Le gestionnaire d’e/s du pilote vérifie que le propriétaire du descripteur de l’appareil dispose d’un accès en lecture/écriture à l’appareil lorsque ce message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="a6aab-122">The driver's I/O manager would check that the owner of the device handle has read/write access to the device when this message is sent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6aab-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6aab-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6aab-124">**Vue d’ensemble de l’application**</span><span class="sxs-lookup"><span data-stu-id="a6aab-124">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="a6aab-125">**IPortableDevice :: Open**</span><span class="sxs-lookup"><span data-stu-id="a6aab-125">**IPortableDevice::Open**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[<span data-ttu-id="a6aab-126">**IPortableDevice::SendCommand**</span><span class="sxs-lookup"><span data-stu-id="a6aab-126">**IPortableDevice::SendCommand**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



