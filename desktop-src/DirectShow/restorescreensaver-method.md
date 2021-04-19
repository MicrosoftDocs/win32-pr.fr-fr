---
description: La méthode DVDAdm. RestoreScreenSaver restaure les paramètres de l’économiseur d’écran système.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Méthode RestoreScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515125"
---
# <a name="restorescreensaver-method"></a><span data-ttu-id="4367b-103">Méthode RestoreScreenSaver</span><span class="sxs-lookup"><span data-stu-id="4367b-103">RestoreScreenSaver Method</span></span>

> [!Note]  
> <span data-ttu-id="4367b-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4367b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4367b-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4367b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4367b-106">La `DVDAdm.RestoreScreenSaver` méthode restaure les paramètres de l’économiseur d’écran système.</span><span class="sxs-lookup"><span data-stu-id="4367b-106">The `DVDAdm.RestoreScreenSaver` method restores the system screen saver settings.</span></span>

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a><span data-ttu-id="4367b-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4367b-107">Return Value</span></span>

<span data-ttu-id="4367b-108">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4367b-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4367b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4367b-109">Remarks</span></span>

<span data-ttu-id="4367b-110">En règle générale, une application DVD désactive l’économiseur d’écran du système au démarrage en affectant à la propriété [**DisableScreenSaver**](disablescreensaver-property.md) la valeur true, puis réactive l’économiseur d’écran lorsque l’application DVD est fermée en appelant `RestoreScreenSaver` .</span><span class="sxs-lookup"><span data-stu-id="4367b-110">Generally, a DVD application will disable the system's screen saver on startup by setting the [**DisableScreenSaver**](disablescreensaver-property.md) property to true, and then re-enable the screen saver again when the DVD application is closed by calling `RestoreScreenSaver`.</span></span> <span data-ttu-id="4367b-111">Si une application n’utilise pas les paramètres d’économiseur d’écran du système, elle n’a pas à appeler cette méthode ou à définir la propriété **DisableScreenSaver** .</span><span class="sxs-lookup"><span data-stu-id="4367b-111">If an application does not use the system's screen saver settings, it does not have to call this method or set the **DisableScreenSaver** property.</span></span>

## <a name="see-also"></a><span data-ttu-id="4367b-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4367b-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4367b-113">Objet MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="4367b-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



