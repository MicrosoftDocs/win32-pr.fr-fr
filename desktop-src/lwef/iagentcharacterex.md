---
title: IAgentCharacterEx
description: IAgentCharacterEx
ms.assetid: 8defc836-cc54-40c7-8afc-ec90f941861b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92a9f9c39804d6b5d3ac777457fff5b7f03823c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227849"
---
# <a name="iagentcharacterex"></a>IAgentCharacterEx

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

**IAgentCharacterEx** dérive de l’interface [**IAgentCharacter**](iagentcharacter.md) . Il inclut toutes les méthodes **IAgentCharacter** et permet d’accéder à des fonctions supplémentaires.

**Méthodes dans l'ordre Vtable**



| Méthodes IAgentCharacterEx                                         | Description                                                                    |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)         | Affiche le menu contextuel du caractère.                                    |
| [**SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)   | Définit si le serveur affiche automatiquement le menu contextuel du caractère.    |
| [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md)   | Retourne une valeur indiquant si le serveur affiche automatiquement le menu contextuel du caractère. |
| [**GetHelpFileName**](iagentcharacterex--gethelpfilename.md)     | Retourne le nom de fichier d’aide pour le caractère.                                   |
| [**SetHelpFileName**](iagentcharacterex--sethelpfilename.md)     | Définit le nom de fichier d’aide pour le caractère.                                      |
| [**SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)         | Définit le mode d’aide sur.                                                             |
| [**GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md)         | Retourne une valeur indiquant si le mode d’aide est activé.                                               |
| [**SetHelpContextID**](iagentcharacterex--sethelpcontextid.md)   | Définit la HelpContextID pour le caractère.                                      |
| [**GetHelpContextID**](iagentcharacterex--gethelpcontextid.md)   | Retourne l’ContexteAide du caractère.                                   |
| [**GetActive**](iagentcharacterex--getactive.md)                 | Retourne l’état actif du caractère.                                    |
| [**Journal**](iagentcharacterex--listen.md)                       | Définit l’état d’écoute pour le caractère.                                    |
| [**SetLanguageID**](iagentcharacterex--setlanguageid.md)         | Définit l’ID de langue du caractère.                                        |
| [**getLanguageID**](iagentcharacterex--getlanguageid.md)         | Retourne l’ID de langue pour le caractère.                                     |
| [**getTTSModeID**](iagentcharacterex--getttsmodeid.md)           | Retourne l’ID de mode TTS défini pour le caractère.                                 |
| [**SetTTSModeID**](iagentcharacterex--setttsmodeid.md)           | Définit l’ID du mode TTS pour le caractère.                                        |
| [**getSRModeID**](iagentcharacterex--getsrmodeid.md)             | Retourne l’ID de mode du moteur de reconnaissance vocale actuel.                       |
| [**setSRModeID**](iagentcharacterex--setsrmodeid.md)             | Définit le moteur de reconnaissance vocale.                                            |
| [**GetGUID**](iagentcharacterex--getguid.md)                     | Retourne l’identificateur du caractère.                                            |
| [**GetOriginalSize**](iagentcharacterex--getoriginalsize.md)     | Retourne la taille d’origine du cadre de caractère.                              |
| [**Réflexion**](iagentcharacterex--think.md)                         | Affiche le texte spécifié dans la bulle « pensée » du caractère.              |
| [**GetVersion**](iagentcharacterex--getversion.md)               | Retourne la version du caractère.                                          |
| [**GetAnimationNames**](iagentcharacterex--getanimationnames.md) | Retourne les noms des animations pour le caractère.                         |
| [**getSRStatus**](iagentcharacterex--getsrstatus.md)             | Retourne les conditions nécessaires pour prendre en charge l’entrée vocale.                      |



 

 

 




