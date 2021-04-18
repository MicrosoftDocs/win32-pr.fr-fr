---
description: 'Quand un appareil est réinitialisé avec succès (IDirect3DDevice9 :: Reset) ou créé (IDirect3D9 :: CreateDevice) dans les opérations en plein écran, l’objet Direct3D qui a créé l’appareil est marqué comme étant propriétaire de tous les adaptateurs sur ce système.'
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Opérations de Multiple-Monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513285"
---
# <a name="multiple-monitor-operations-direct3d-9"></a><span data-ttu-id="b30af-103">Opérations de Multiple-Monitor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b30af-103">Multiple-Monitor Operations (Direct3D 9)</span></span>

<span data-ttu-id="b30af-104">Quand un appareil est réinitialisé avec succès ([**IDirect3DDevice9 :: Reset**](/windows/desktop/api)) ou créé ([**IDirect3D9 :: CreateDevice**](/windows/desktop/api)) dans les opérations en plein écran, l’objet Direct3D qui a créé l’appareil est marqué comme étant propriétaire de tous les adaptateurs sur ce système.</span><span class="sxs-lookup"><span data-stu-id="b30af-104">When a device is successfully reset ([**IDirect3DDevice9::Reset**](/windows/desktop/api)) or created ([**IDirect3D9::CreateDevice**](/windows/desktop/api)) in full-screen operations, the Direct3D object that created the device is marked as owning all adapters on that system.</span></span> <span data-ttu-id="b30af-105">Cet État est appelé mode exclusif et l’objet Direct3D est propriétaire du mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="b30af-105">This state is known as exclusive mode, and the Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="b30af-106">Le mode exclusif signifie que les appareils créés par tout autre objet Direct3D ne peuvent ni assumer les opérations en plein écran, ni allouer de la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="b30af-106">Exclusive mode means that devices created by any other Direct3D object can neither assume full-screen operations nor allocate video memory.</span></span> <span data-ttu-id="b30af-107">En outre, lorsqu’un objet Direct3D suppose le mode exclusif, tous les appareils autres que celui qui s’est déroulé en plein écran sont placés dans un état perdu.</span><span class="sxs-lookup"><span data-stu-id="b30af-107">In addition, when a Direct3D object assumes exclusive mode, all devices other than the one that went full-screen are placed in lost state.</span></span> <span data-ttu-id="b30af-108">Pour plus d’informations, consultez [appareils perdus (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b30af-108">For details, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="b30af-109">En même temps que le mode exclusif, l’objet Direct3D est informé de la fenêtre de focus que l’appareil utilisera.</span><span class="sxs-lookup"><span data-stu-id="b30af-109">Along with exclusive mode, the Direct3D object is informed of the focus window that the device will use.</span></span> <span data-ttu-id="b30af-110">Le mode exclusif est relâché quand l’appareil plein écran final détenu par cet objet Direct3D est réinitialisé en mode fenêtre ou détruit.</span><span class="sxs-lookup"><span data-stu-id="b30af-110">Exclusive mode is released when the final full-screen device owned by that Direct3D object is either reset to windowed mode or destroyed.</span></span>

<span data-ttu-id="b30af-111">Les appareils peuvent être divisés en deux catégories lorsqu’un objet Direct3D est propriétaire du mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="b30af-111">Devices can be divided into two categories when a Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="b30af-112">La première catégorie d’appareils a les caractéristiques suivantes.</span><span class="sxs-lookup"><span data-stu-id="b30af-112">The first category of devices have the following characteristics.</span></span>

-   <span data-ttu-id="b30af-113">Ils sont créés par le même objet Direct3D qui a créé l’appareil en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="b30af-113">They are created by the same Direct3D object that created the device that is full-screen.</span></span>
-   <span data-ttu-id="b30af-114">Ils ont la même fenêtre de focus que l’appareil plein écran.</span><span class="sxs-lookup"><span data-stu-id="b30af-114">They have the same focus window as the device that is full-screen.</span></span>
-   <span data-ttu-id="b30af-115">Ils représentent un adaptateur différent à partir de n’importe quel appareil plein écran.</span><span class="sxs-lookup"><span data-stu-id="b30af-115">They represent a different adapter from any full-screen device.</span></span>

<span data-ttu-id="b30af-116">Les appareils de cette catégorie n’ont aucune restriction quant à leur capacité de réinitialisation ou de création, et ils ne sont pas placés dans un état perdu.</span><span class="sxs-lookup"><span data-stu-id="b30af-116">Devices in this category have no restrictions concerning their ability to be reset or created, and they are not placed in lost state.</span></span> <span data-ttu-id="b30af-117">Les appareils de cette catégorie peuvent même être mis en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="b30af-117">Devices in this category can even be put into full-screen mode.</span></span>

<span data-ttu-id="b30af-118">Les appareils qui ne se trouvent pas dans la première catégorie-les appareils créés par un autre objet Direct3D, créés avec une fenêtre de focus différente, et créés pour un adaptateur avec un appareil qui est déjà plein écran, ne peuvent pas être réinitialisés et restent en état de perte tant que le mode exclusif n’est pas perdu.</span><span class="sxs-lookup"><span data-stu-id="b30af-118">Devices that do not fall in the first category - devices created by another Direct3D object, created with a different focus window, and created for an adapter with a device that is already full-screen - cannot be reset and remain in lost state until the exclusive mode is lost.</span></span> <span data-ttu-id="b30af-119">Par conséquent, une application à plusieurs moniteurs peut placer plusieurs appareils en mode plein écran, mais uniquement si tous ces appareils sont destinés à des adaptateurs différents, ont été créés par le même objet Direct3D et partagent la même fenêtre de focus.</span><span class="sxs-lookup"><span data-stu-id="b30af-119">As a result, a multiple-monitor application can place several devices in full-screen mode, but only if all these devices are for different adapters, were created by the same Direct3D object, and share the same focus window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b30af-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b30af-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b30af-121">Présentation d’une scène</span><span class="sxs-lookup"><span data-stu-id="b30af-121">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 



