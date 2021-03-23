---
title: Gestion des erreurs et de la suppression des appareils dans DirectML
description: Cette rubrique explique comment déboguer la suppression de l’appareil DirectML et d’autres conditions d’erreur.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548540"
---
# <a name="handling-errors-and-device-removal-in-directml"></a><span data-ttu-id="89b45-103">Gestion des erreurs et de la suppression des appareils dans DirectML</span><span class="sxs-lookup"><span data-stu-id="89b45-103">Handling errors and device-removal in DirectML</span></span>

## <a name="device-removal"></a><span data-ttu-id="89b45-104">Appareil-suppression</span><span class="sxs-lookup"><span data-stu-id="89b45-104">Device-removal</span></span>

<span data-ttu-id="89b45-105">Si une erreur irrécupérable se produit, l’appareil DirectML peut entrer un État « appareil supprimé ».</span><span class="sxs-lookup"><span data-stu-id="89b45-105">If an unrecoverable error occurs, the DirectML device may enter a "device-removed" state.</span></span> <span data-ttu-id="89b45-106">Les erreurs irrécupérables qui provoquent la suppression de l’appareil incluent une utilisation d’API non valide (pour les méthodes qui ne retournent pas de [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), une erreur de pilote, une défaillance matérielle ou des conditions de mémoire insuffisante (insuffisance).</span><span class="sxs-lookup"><span data-stu-id="89b45-106">Unrecoverable errors that cause device-removal include invalid API usage (for methods that don't return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), driver error, hardware fault, or out-of-memory (OOM) conditions.</span></span>

<span data-ttu-id="89b45-107">Lorsqu’un appareil DirectML est supprimé, tous les appels de méthode sur l’appareil et tous les objets créés par ce périphérique deviennent non-OPS.</span><span class="sxs-lookup"><span data-stu-id="89b45-107">When a DirectML device is removed, all method calls on the device, and every object created by that device, become no-ops.</span></span> <span data-ttu-id="89b45-108">Pour les méthodes qui retournent un [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), un code d’erreur [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) est retourné.</span><span class="sxs-lookup"><span data-stu-id="89b45-108">For methods that return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), a [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) error code is returned.</span></span> <span data-ttu-id="89b45-109">Vous pouvez utiliser la [méthode **IDMLDevice :: GetDeviceRemovedReason**](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) pour vérifier si l’appareil DirectML a été supprimé et pour récupérer un code d’erreur plus détaillé.</span><span class="sxs-lookup"><span data-stu-id="89b45-109">You can use the [**IDMLDevice::GetDeviceRemovedReason** method](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) to check whether the DirectML device has been removed, and to retrieve a more detailed error code.</span></span>

<span data-ttu-id="89b45-110">Vous ne pouvez pas récupérer à partir de la suppression de l’appareil, sauf en libérant l’appareil affecté et tous ses enfants, puis en recréant l’appareil DirectML à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="89b45-110">You can't recover from device-removal except by releasing the affected device and all its children, then re-creating the DirectML device from scratch.</span></span>

<span data-ttu-id="89b45-111">L’appareil : la suppression de l’appareil Direct3D 12 sous-jacent entraîne également la suppression de l’appareil DirectML.</span><span class="sxs-lookup"><span data-stu-id="89b45-111">Device-removal of the underlying Direct3D 12 device also causes the DirectML device to be removed.</span></span> <span data-ttu-id="89b45-112">En revanche, l'inverse n'est pas vrai.</span><span class="sxs-lookup"><span data-stu-id="89b45-112">However, the reverse is not true.</span></span> <span data-ttu-id="89b45-113">DirectML : la suppression de l’appareil ne peut pas nécessairement entraîner la suppression de l’appareil Direct3D 12 sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="89b45-113">DirectML device-removal may not necessarily cause the underlying Direct3D 12 device to become removed.</span></span>

## <a name="debugging-directml-device-removal-and-other-errors"></a><span data-ttu-id="89b45-114">Débogage de l’appareil DirectML-suppression et autres erreurs</span><span class="sxs-lookup"><span data-stu-id="89b45-114">Debugging DirectML device-removal, and other errors</span></span>

<span data-ttu-id="89b45-115">La cause la plus courante des erreurs DirectML est l’utilisation d’API non valide.</span><span class="sxs-lookup"><span data-stu-id="89b45-115">The most common cause of DirectML errors is invalid API usage.</span></span> <span data-ttu-id="89b45-116">Une utilisation d’API non valide peut entraîner un **E_INVALIDARG** code d’erreur HRESULT, ou peut entraîner la suppression de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="89b45-116">Invalid API usage might result in an **E_INVALIDARG** HRESULT error code, or it might result in device-removal.</span></span>

<span data-ttu-id="89b45-117">Nous vous recommandons vivement d’activer la [couche de débogage DirectML](dml-debug-layer.md) pendant votre développement, afin d’intercepter et de déboguer ces erreurs.</span><span class="sxs-lookup"><span data-stu-id="89b45-117">We strongly recommend that you enable the [DirectML debug layer](dml-debug-layer.md) during your development, in order to catch and debug such errors.</span></span> <span data-ttu-id="89b45-118">La couche de débogage DirectML effectue une validation complète des paramètres de méthode et de l’utilisation des API, et émet des messages de sortie de débogage pour vous aider à effectuer le débogage.</span><span class="sxs-lookup"><span data-stu-id="89b45-118">The DirectML debug layer performs extensive validation of method parameters and API usage, and it will emit debug output messages to help you debug.</span></span>

## <a name="see-also"></a><span data-ttu-id="89b45-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89b45-119">See also</span></span>

* [<span data-ttu-id="89b45-120">Utilisation de la couche de débogage DirectML</span><span class="sxs-lookup"><span data-stu-id="89b45-120">Using the DirectML debug layer</span></span>](dml-debug-layer.md)
