---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036e1d41878adaae878a5961b45d190971d790af
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119004"
---
# <a name="iagentcharacterexsetlanguageid"></a>IAgentCharacterEx::SetLanguageID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

Définit l’ID de langue défini pour le caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Paramètre de l’ID de langue pour le caractère.

</dd> </dl>

Entier long spécifiant l’ID de langue du caractère. L’ID de langue (LANGID) d’un caractère est une valeur de 16 bits définie par Windows, composée d’un ID de langue primaire et d’un ID de langue secondaire. Vous pouvez utiliser les valeurs suivantes pour les langues spécifiées. Pour plus d’informations, consultez la documentation du kit de développement Platform SDK.



| Langage              | id     |  Langage             | id     |
|-----------------------|--------|-----------------------|--------|
| Arabe (Arabie)        | 0x0401 | Italien               | 0x0410 |
| Basque                | 0x042d | Japonais              | 0x0411 |
| Chinois (simplifié)  | 0x0804 | Coréen                | 0x0412 |
| Chinois (traditionnel) | 0x0404 | Norvégien             | 0x0414 |
| Croate              | 0x041A | Polonais                | 0x0415 |
| Tchèque                 | 0x0405 | Portugais (Portugal) | 0x0816 |
| Danois                | 0x0406 | Portugais (Brésil)   | 0x0416 |
| Néerlandais                 | 0x0413 | Roumain              | 0x0418 |
| Anglais (Royaume-Uni)     | 0x0809 | Russe               | 0x0419 |
| Anglais (US)          | 0x0409 | Slovaque             | 0x041B |
| Finnois               | 0x040B | Slovène             | 0x0424 |
| Français                | 0x040C | Espagnol               | 0x0C0A |
| Allemand                | 0x0407 | Suédois               | 0x041D |
| Grec                 | 0x0408 | Thaï                  | 0x041E |
| Hébreu                | 0x040D | Turc               | 0x041F |
| Hongrois             | 0x040E |                       |        |



 

Si vous ne définissez pas l’ID de langue pour le caractère, son ID de langue sera l’ID de langue actuel du système si la DLL de langue de l’agent correspondante est installée. dans le cas contraire, la langue du caractère sera l’anglais (États-Unis).

Cette propriété détermine également la langue du texte de la bulle, les commandes du menu contextuel du caractère et le moteur de reconnaissance vocale. Elle détermine également la langue par défaut de la sortie TTS. Pour déterminer si un moteur vocal compatible est disponible pour la langue du caractère, utilisez [**IAgentCharacterEx :: GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx :: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).

Si vous essayez de définir l’ID de langue d’un caractère et les ressources linguistiques de l’agent, la page de codes ou une police d’affichage pour l’ID de langue n’est pas disponible, l’agent retourne une erreur et l’ID de langue du caractère reste le dernier paramètre. La définition de cette propriété ne retourne pas d’erreur s’il n’existe aucun moteur de reconnaissance vocale correspondant à la langue.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

> [!Note]  
> Si vous définissez l’ID de langue du caractère sur une langue qui prend en charge le texte bidirectionnel (tel que l’arabe ou l’hébreu), mais que le système qui exécute votre application n’a pas de prise en charge bidirectionnelle installée, le texte apparaît dans le mot-bulle dans l’ordre logique plutôt que dans l’ordre d’affichage.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx : GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx :: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx :: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




