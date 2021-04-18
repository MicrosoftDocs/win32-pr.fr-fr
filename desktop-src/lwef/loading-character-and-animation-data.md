---
title: Chargement des données de caractères et d’animation
description: Chargement des données de caractères et d’animation
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed77524c4e3cbbcae725b87c3671914f2261fa1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106540747"
---
# <a name="loading-character-and-animation-data"></a><span data-ttu-id="f39dc-103">Chargement des données de caractères et d’animation</span><span class="sxs-lookup"><span data-stu-id="f39dc-103">Loading Character and Animation Data</span></span>

<span data-ttu-id="f39dc-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f39dc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f39dc-105">Une fois que vous avez un pointeur vers l’interface [**IAgentEx**](iagentex.md) , vous pouvez utiliser la méthode [**Load**](load-method.md) pour charger un caractère et récupérer son interface [**IAgentCharacterEx**](iagentcharacterex.md) .</span><span class="sxs-lookup"><span data-stu-id="f39dc-105">After you have a pointer to the [**IAgentEx**](iagentex.md) interface, you can use the [**Load**](load-method.md) method to load a character and retrieve its [**IAgentCharacterEx**](iagentcharacterex.md) interface.</span></span> <span data-ttu-id="f39dc-106">Il existe trois possibilités différentes pour le chemin de chargement d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="f39dc-106">There are three different possibilities for the Load path of a character.</span></span> <span data-ttu-id="f39dc-107">Le premier est compatible avec l’agent Microsoft 1,5 où le chemin d’accès spécifié est le chemin d’accès complet et le nom de fichier d’un fichier de caractères.</span><span class="sxs-lookup"><span data-stu-id="f39dc-107">The first is compatible with Microsoft Agent 1.5 where the specified path is the full path and filename of a character file.</span></span> <span data-ttu-id="f39dc-108">La seconde possibilité consiste à spécifier uniquement le nom de fichier, auquel cas l’agent recherche dans son répertoire de caractères.</span><span class="sxs-lookup"><span data-stu-id="f39dc-108">The second possibility is to specify the filename only, in which case, Agent looks in its Chars directory.</span></span> <span data-ttu-id="f39dc-109">La dernière possibilité consiste à fournir un paramètre Variant vide qui entraîne le chargement du caractère par défaut.</span><span class="sxs-lookup"><span data-stu-id="f39dc-109">The last possibility is to supply an empty Variant parameter that causes the default character to be loaded.</span></span>


```
   // Create a variant to store the filename of the character to load

   const LPWSTR kpwszCharacter = L"merlin.acs";

   VariantInit(&vPath);

   vPath.vt = VT_BSTR;
   vPath.bstrVal = SysAllocString(kpwszCharacter);

   // Load the character

   hRes = pAgentEx->Load(vPath, &lCharID, &lRequestID);

   // Get its IAgentCharacterEx interface

   hRes = pAgentEx->GetCharacterEx(lCharID, &pCharacterEx);
```



<span data-ttu-id="f39dc-110">Vous pouvez utiliser cette interface pour accéder aux méthodes du caractère :</span><span class="sxs-lookup"><span data-stu-id="f39dc-110">You can use this interface to access the character's methods:</span></span>


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



<span data-ttu-id="f39dc-111">Lorsque vous n’avez plus besoin des services Microsoft Agent, par exemple lorsque votre application cliente s’arrête, libérez ses interfaces.</span><span class="sxs-lookup"><span data-stu-id="f39dc-111">When you no longer need Microsoft Agent services, such as when your client application shuts down, release its interfaces.</span></span> <span data-ttu-id="f39dc-112">Notez que la libération de l’interface de caractères ne décharge pas le caractère.</span><span class="sxs-lookup"><span data-stu-id="f39dc-112">Note that releasing the character interface does not unload the character.</span></span> <span data-ttu-id="f39dc-113">Appelez la méthode [**Unload**](unload-method.md) pour effectuer cette opération avant de libérer l’interface [**IAgentEx**](iagentex.md) :</span><span class="sxs-lookup"><span data-stu-id="f39dc-113">Call the [**Unload**](unload-method.md) method to do this before releasing the [**IAgentEx**](iagentex.md) interface:</span></span>


```
// Clean up

if (pCharacterEx) {

   // Release the character interface

   pCharacterEx->Release();

   // Unload the character.  NOTE:  releasing the character
   // interface does NOT make the character go away.  You must
   // call Unload.

   pAgentEx->Unload(lCharID);
}
   
// Release the Agent

pAgentEx->Release();

VariantClear(&vPath);
```



 

 




