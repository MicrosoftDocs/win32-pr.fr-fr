---
description: Pour qu’une application puisse ajouter des données au registre, elle doit créer ou ouvrir une clé.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Ouverture, création et fermeture de clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3260c255240ce2c7fb5d13fe28126a1a3f5527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524903"
---
# <a name="opening-creating-and-closing-keys"></a><span data-ttu-id="e4553-103">Ouverture, création et fermeture de clés</span><span class="sxs-lookup"><span data-stu-id="e4553-103">Opening, Creating, and Closing Keys</span></span>

<span data-ttu-id="e4553-104">Pour qu’une application puisse ajouter des données au registre, elle doit créer ou ouvrir une clé.</span><span class="sxs-lookup"><span data-stu-id="e4553-104">Before an application can add data to the registry, it must create or open a key.</span></span> <span data-ttu-id="e4553-105">Pour créer ou ouvrir une clé, une application fait toujours référence à la clé en tant que sous-clé d’une clé actuellement ouverte.</span><span class="sxs-lookup"><span data-stu-id="e4553-105">To create or open a key, an application always refers to the key as a subkey of a currently open key.</span></span> <span data-ttu-id="e4553-106">Les clés prédéfinies suivantes sont toujours ouvertes : **HKEY \_ local \_ machine**, **HKEY \_ classes \_ root**, **HKEY \_ Users** et **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="e4553-106">The following predefined keys are always open: **HKEY\_LOCAL\_MACHINE**, **HKEY\_CLASSES\_ROOT**, **HKEY\_USERS**, and **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="e4553-107">Une application utilise la fonction [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) pour ouvrir une clé et la fonction [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) pour créer une clé.</span><span class="sxs-lookup"><span data-stu-id="e4553-107">An application uses the [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) function to open a key and the [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) function to create a key.</span></span> <span data-ttu-id="e4553-108">Une arborescence du Registre peut avoir 512 niveaux de profondeur.</span><span class="sxs-lookup"><span data-stu-id="e4553-108">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="e4553-109">Vous pouvez créer jusqu’à 32 niveaux à la fois à l’aide d’un appel d’API de Registre unique.</span><span class="sxs-lookup"><span data-stu-id="e4553-109">You can create up to 32 levels at a time through a single registry API call.</span></span>

<span data-ttu-id="e4553-110">Une application peut utiliser la fonction [**échec RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) pour fermer une clé et écrire les données qu’elle contient dans le registre.</span><span class="sxs-lookup"><span data-stu-id="e4553-110">An application can use the [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) function to close a key and write the data it contains into the registry.</span></span> <span data-ttu-id="e4553-111">**Échec RegCloseKey** n’écrit pas nécessairement les données dans le registre avant de retourner. le vidage du cache sur le disque dur peut prendre jusqu’à plusieurs secondes.</span><span class="sxs-lookup"><span data-stu-id="e4553-111">**RegCloseKey** does not necessarily write the data to the registry before returning; it can take as much as several seconds for the cache to be flushed to the hard disk.</span></span> <span data-ttu-id="e4553-112">Si une application doit écrire explicitement des données du Registre sur le disque dur, elle peut utiliser la fonction [**regflushkey a**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) .</span><span class="sxs-lookup"><span data-stu-id="e4553-112">If an application must explicitly write registry data to the hard disk, it can use the [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) function.</span></span> <span data-ttu-id="e4553-113">Toutefois, **regflushkey a** utilise de nombreuses ressources système et doit être appelé uniquement lorsque cela est absolument nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e4553-113">**RegFlushKey**, however, uses many system resources and should be called only when absolutely necessary.</span></span>

 

 



