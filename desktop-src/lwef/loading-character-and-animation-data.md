---
title: Chargement des données de caractères et d’animation
description: Chargement des données de caractères et d’animation
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e387a6122ab08513763878678d99941ef65d8ed11822eed8639fccd6e3815d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961429"
---
# <a name="loading-character-and-animation-data"></a>Chargement des données de caractères et d’animation

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Une fois que vous avez un pointeur vers l’interface [**IAgentEx**](iagentex.md) , vous pouvez utiliser la méthode [**Load**](load-method.md) pour charger un caractère et récupérer son interface [**IAgentCharacterEx**](iagentcharacterex.md) . Il existe trois possibilités différentes pour le chemin de chargement d’un caractère. Le premier est compatible avec l’agent Microsoft 1,5 où le chemin d’accès spécifié est le chemin d’accès complet et le nom de fichier d’un fichier de caractères. La seconde possibilité consiste à spécifier uniquement le nom de fichier, auquel cas l’agent recherche dans son répertoire de caractères. La dernière possibilité consiste à fournir un paramètre Variant vide qui entraîne le chargement du caractère par défaut.


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



Vous pouvez utiliser cette interface pour accéder aux méthodes du caractère :


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



Lorsque vous n’avez plus besoin des services Microsoft Agent, par exemple lorsque votre application cliente s’arrête, libérez ses interfaces. Notez que la libération de l’interface de caractères ne décharge pas le caractère. Appelez la méthode [**Unload**](unload-method.md) pour effectuer cette opération avant de libérer l’interface [**IAgentEx**](iagentex.md) :


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



 

 




