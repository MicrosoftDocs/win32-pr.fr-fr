---
title: À propos de l’objet Settings
description: À propos de l’objet Settings
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player, objet Settings
- Modèle d’objet du lecteur Windows Media, objet paramètres
- modèle objet, objet Settings
- Contrôle ActiveX du lecteur Windows Media, objet paramètres
- Contrôle ActiveX, objet Settings
- Contrôle ActiveX Windows Media Player Mobile, paramètres (objet)
- Windows Media Player Mobile, objet Settings
- Settings (objet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839453"
---
# <a name="about-the-settings-object"></a><span data-ttu-id="90c14-111">À propos de l’objet Settings</span><span class="sxs-lookup"><span data-stu-id="90c14-111">About the Settings Object</span></span>

<span data-ttu-id="90c14-112">L’objet **Settings** régit les paramètres du contrôle tels que volume, Play Count, MUTE, etc.</span><span class="sxs-lookup"><span data-stu-id="90c14-112">The **Settings** object governs the settings of the control such as volume, play count, mute, and so on.</span></span> <span data-ttu-id="90c14-113">Elle est accessible uniquement par le biais de la propriété **Settings** de l’objet **Player** .</span><span class="sxs-lookup"><span data-stu-id="90c14-113">It is accessed only through the **Settings** property of the **Player** object.</span></span> <span data-ttu-id="90c14-114">La propriété **Settings** retourne l’objet **Settings** .</span><span class="sxs-lookup"><span data-stu-id="90c14-114">The **Settings** property returns the **Settings** object.</span></span> <span data-ttu-id="90c14-115">Vous pouvez uniquement accéder aux propriétés de l’objet **Settings** après l’avoir créé.</span><span class="sxs-lookup"><span data-stu-id="90c14-115">You can only access the properties of the **Settings** object after you have created it.</span></span> <span data-ttu-id="90c14-116">Par exemple, pour obtenir la valeur de la propriété **volume** , vous devez utiliser le code suivant :</span><span class="sxs-lookup"><span data-stu-id="90c14-116">For example, to get the value of the **Volume** property, you must use the following code:</span></span>


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a><span data-ttu-id="90c14-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90c14-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90c14-118">**Modèle objet de lecteur pour les langages de script**</span><span class="sxs-lookup"><span data-stu-id="90c14-118">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="90c14-119">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="90c14-119">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 




