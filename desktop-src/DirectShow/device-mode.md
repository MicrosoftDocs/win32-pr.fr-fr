---
description: Modèle d’appareil
ms.assetid: d56021be-616b-41cd-8cf0-9e0d314f62cd
title: Modèle d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4657fbb49e2619d75911c18185109805116b9647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482704"
---
# <a name="device-mode"></a><span data-ttu-id="89d42-103">Modèle d’appareil</span><span class="sxs-lookup"><span data-stu-id="89d42-103">Device Mode</span></span>

<span data-ttu-id="89d42-104">Les caméscopes IEEE 1394 et USB peuvent basculer entre le mode caméra et le mode magnétoscope (magnétoscope).</span><span class="sxs-lookup"><span data-stu-id="89d42-104">IEEE 1394 and USB camcorders can switch between camera mode and video tape recorder (VTR) mode.</span></span> <span data-ttu-id="89d42-105">Quand un caméscope IEEE 1394 change de mode, le périphérique est redéfini et l’application doit l’énumérer à nouveau.</span><span class="sxs-lookup"><span data-stu-id="89d42-105">When an IEEE 1394 camcorder switches modes, the device resets and the application must enumerate it again.</span></span> <span data-ttu-id="89d42-106">Il n’existe aucun moyen pour une application de basculer le mode par programme.</span><span class="sxs-lookup"><span data-stu-id="89d42-106">There is no way for an application to switch the mode programmatically.</span></span> <span data-ttu-id="89d42-107">Les caméscopes USB, quant à eux, peuvent basculer entre les modes caméra et magnétoscope sans réinitialiser, et l’application peut modifier le mode.</span><span class="sxs-lookup"><span data-stu-id="89d42-107">USB camcorders, on the other hand, can switch between camera and VTR modes without resetting, and the application can change the mode.</span></span>

<span data-ttu-id="89d42-108">**Pilote MSDV**</span><span class="sxs-lookup"><span data-stu-id="89d42-108">**MSDV Driver**</span></span>

<span data-ttu-id="89d42-109">Pour récupérer le mode actuel sur un appareil IEEE 1394, appelez la méthode [**IAMExtDevice :: GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) avec la valeur Ed \_ DEVCAP \_ Device \_ type.</span><span class="sxs-lookup"><span data-stu-id="89d42-109">To get the current mode on an IEEE 1394 device, call the [**IAMExtDevice::GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) method with the value ED\_DEVCAP\_DEVICE\_TYPE.</span></span> <span data-ttu-id="89d42-110">Si la méthode retourne le \_ magnétoscope devtype de valeur Ed \_ , l’appareil est en mode VTR et possède des fonctions telles que pause, arrêt, avance rapide et rembobiner.</span><span class="sxs-lookup"><span data-stu-id="89d42-110">If the method returns the value ED\_DEVTYPE\_VCR, the device is in VTR mode and has functions such as pause, stop, fast-forward, and rewind.</span></span> <span data-ttu-id="89d42-111">Sinon, si la méthode retourne ED \_ devtype \_ Camera, l’appareil est en mode caméra.</span><span class="sxs-lookup"><span data-stu-id="89d42-111">Otherwise, if the method returns ED\_DEVTYPE\_CAMERA, the device is in camera mode.</span></span> <span data-ttu-id="89d42-112">L’exemple de code suivant montre comment interroger le type d’appareil :</span><span class="sxs-lookup"><span data-stu-id="89d42-112">The following code example shows how to query the device type:</span></span>


```C++
if (MyDevCap.bHasDevice) 
{
    LONG lDeviceType = 0;
    MyDevCap.pDevice->GetCapability(ED_DEVCAP_DEVICE_TYPE, &lDeviceType, 0);

    if (lDeviceType == ED_DEVTYPE_VCR) 
    {
        // Device is a VTR. Enable all VTR functions.
    }
    else 
    {
        // Device is a camera. 
        // Enable record and record-pause; disable other functions.
    }
}
```



<span data-ttu-id="89d42-113">Si le caméscope passe en mode hors connexion, vous devez le demander une nouvelle fois dès qu’il sera disponible.</span><span class="sxs-lookup"><span data-stu-id="89d42-113">If the camcorder goes offline, you should query it again when it next becomes available.</span></span> <span data-ttu-id="89d42-114">Le gestionnaire de graphique de filtre publie un événement de [**\_ \_ perte d’appareil ce**](ec-device-lost.md) lorsque l’appareil est supprimé.</span><span class="sxs-lookup"><span data-stu-id="89d42-114">The filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event when the device is removed.</span></span>

<span data-ttu-id="89d42-115">**Pilote UVC**</span><span class="sxs-lookup"><span data-stu-id="89d42-115">**UVC Driver**</span></span>

<span data-ttu-id="89d42-116">Étant donné que les périphériques vidéo USB peuvent changer de mode sans réinitialiser, le code présenté dans les exemples précédents n’est pas fiable pour les périphériques USB.</span><span class="sxs-lookup"><span data-stu-id="89d42-116">Because USB video devices can switch modes without resetting, the code shown in the previous examples is not reliable for USB devices.</span></span> <span data-ttu-id="89d42-117">Utilisez plutôt l’interface [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) pour accéder au mode actuel.</span><span class="sxs-lookup"><span data-stu-id="89d42-117">Instead, use the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface to get the current mode.</span></span> <span data-ttu-id="89d42-118">Vous pouvez également utiliser cette interface pour changer de mode par programme si l’appareil la prend en charge.</span><span class="sxs-lookup"><span data-stu-id="89d42-118">You can also use this interface to switch modes programmatically if the device supports it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89d42-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89d42-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89d42-120">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="89d42-120">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



