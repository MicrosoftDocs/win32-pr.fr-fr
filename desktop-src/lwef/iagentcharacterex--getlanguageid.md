---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0eeee052111ef0acbb843f4362ca0bfd3b40ab7d154ef0c46c43f6c2d0e0f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105547"
---
# <a name="iagentcharacterexgetlanguageid"></a>IAgentCharacterEx::GetLanguageID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

Récupère l’ID de langue défini pour le caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*
</dt> <dd>

Adresse d’une variable qui reçoit le paramètre ID de langue pour le caractère.

</dd> </dl>

Entier long spécifiant l’ID de langue du caractère. l’id de langue (LANGID) d’un caractère est une valeur de 16 bits définie par Windows, composée d’un id de langue primaire et d’un id de langue secondaire. Les exemples suivants sont des valeurs pour certains langages. Pour déterminer les valeurs d’autres langages, consultez la documentation du kit de développement Platform SDK.



| Langage              | ID     | Langage              | ID     |
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
| Anglais (États-Unis)          | 0x0409 | Slovaque             | 0x041B |
| Finnois               | 0x040B | Slovène             | 0x0424 |
| Français                | 0x040C | Espagnol               | 0x0C0A |
| Allemand                | 0x0407 | Suédois               | 0x041D |
| Grec                 | 0x0408 | Thaï                  | 0x041E |
| Hébreu                | 0x040D | Turc               | 0x041F |
| Hongrois             | 0x040E |                       |        |



 

Si vous ne définissez pas cet ID de langue pour le caractère, l’ID de langue du caractère sera l’ID de langue du système actuel.

Ce paramètre détermine également la langue pour la sortie TTS, le texte de la bulle, les commandes dans le menu contextuel du caractère et le moteur de reconnaissance vocale. Pour déterminer si un moteur de reconnaissance vocale compatible est disponible pour la langue du caractère, utilisez [**IAgentCharacterEx :: GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx :: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

> [!Note]  
> Si l’ID de langue est défini sur une langue qui prend en charge le texte bidirectionnel (comme l’arabe ou l’hébreu), mais que le système qui exécute votre application n’a pas de prise en charge bidirectionnelle installée, le texte apparaît dans le mot-bulle dans l’ordre logique plutôt que dans l’ordre d’affichage.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx : SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx :: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx :: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




