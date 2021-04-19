---
description: Une fois que vous avez créé une extension de composant logiciel enfichable d’attachement, vous devez l’inscrire pour que la console MMC et les composants logiciels enfichables de configuration de la sécurité la localisent et l’utilisent.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Inscription d’une extension de composant logiciel enfichable pièce jointe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514597"
---
# <a name="registering-an-attachment-snap-in-extension"></a><span data-ttu-id="61436-103">Inscription d’une extension de composant logiciel enfichable pièce jointe</span><span class="sxs-lookup"><span data-stu-id="61436-103">Registering an Attachment Snap-in Extension</span></span>

<span data-ttu-id="61436-104">Une fois que vous avez créé une extension de composant logiciel enfichable d’attachement, vous devez l’inscrire pour que la console MMC et les composants logiciels enfichables de configuration de la sécurité la localisent et l’utilisent.</span><span class="sxs-lookup"><span data-stu-id="61436-104">After you create an attachment snap-in extension, you must register it in order for the MMC and the Security Configuration snap-ins to locate and use it.</span></span>

<span data-ttu-id="61436-105">Le composant logiciel enfichable de votre pièce jointe doit étendre l’espace de noms des composants logiciels enfichables de configuration de sécurité en ajoutant son propre nœud, comme décrit dans la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="61436-105">Your attachment snap-in must extend the Security Configuration snap-ins namespace by adding its own node as described in the following procedure.</span></span>

<span data-ttu-id="61436-106">**Pour installer et inscrire l’extension du composant logiciel enfichable pièce jointe**</span><span class="sxs-lookup"><span data-stu-id="61436-106">**To install and register the attachment snap-in extension**</span></span>

1.  <span data-ttu-id="61436-107">Enregistrez l’extension du composant logiciel enfichable sous la clé de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="61436-107">Register the snap-in extension under the following registry key.</span></span> <span data-ttu-id="61436-108">Ne créez pas de clé autonome sous le composant logiciel enfichable. les extensions des composants logiciels enfichables d’attachement doivent uniquement être des extensions.</span><span class="sxs-lookup"><span data-stu-id="61436-108">Do not create a StandAlone key under the snap-in; attachment snap-ins extensions must only be extensions.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  <span data-ttu-id="61436-109">Enregistrez l’extension du composant logiciel enfichable d’attachement sous les sous-clés suivantes.</span><span class="sxs-lookup"><span data-stu-id="61436-109">Register the attachment snap-in extension under the following subkeys.</span></span> <span data-ttu-id="61436-110">Cela peut être fait dans le cadre de vos implémentations de fonction **DllRegisterServer** et **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="61436-110">This can be done as part of your **DllRegisterServer** and **DllUnregisterServer** function implementations.</span></span>

    <span data-ttu-id="61436-111">Espace de noms [modèles de sécurité](security-templates.md) :</span><span class="sxs-lookup"><span data-stu-id="61436-111">[Security Templates](security-templates.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    <span data-ttu-id="61436-112">Espace de noms d' [analyse et de configuration de la sécurité](security-configuration-and-analysis.md) :</span><span class="sxs-lookup"><span data-stu-id="61436-112">[Security Configuration and Analysis](security-configuration-and-analysis.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



