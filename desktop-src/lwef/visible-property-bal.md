---
title: Visible, propriété (objet Balloon)
description: Propriété visible
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba58993a3328a4c99dbe7da43b43460f6048bf57
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032161"
---
# <a name="visible-property-balloon-object"></a>Visible, propriété (objet Balloon)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit le paramètre visible pour le mot-bulle pour le caractère spécifié.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe** 
</dt> <dd>

*agent ***. Caractères (**"* CharacterID *" * *).* *  \[  =  *Valeur booléenne* Balloon. visible\]



| Partie      | Description                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expression booléenne spécifiant si la bulle de texte est visible.<br/> **True** La bulle est visible.<br/> **Valeur false** La bulle est masquée.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Si vous suivez un appel [**Speak**](speak-method.md) ou [**Song**](think-method.md) avec une instruction pour tenter de modifier la propriété de l’info-bulle, cela peut ne pas affecter l’état visible de l’info-bulle, car l’appel **Speak** ou **Song** est mis en file d’attente, mais pas l’appel de la définition de l’état visible de l’info-bulle. Par conséquent, définissez cette valeur uniquement quand aucun appel **Speak** ou **Song** n’est présent dans la file d’attente du caractère.

Si vous tentez de définir cette propriété alors que le caractère parle, bouge ou est glissé, le paramètre de la propriété ne prend pas effet tant que l’opération précédente n’est pas terminée.

L’appel des méthodes [**Speak**](speak-method.md) et [**Song**](think-method.md) rend automatiquement la bulle visible, en affectant la **valeur true** à la propriété [**visible**](visible-property.md) . Si la propriété de masquage automatique de l’info-bulle du caractère est activée, l’info-bulle est automatiquement masquée une fois que le texte de sortie est prononcé. Le fait de cliquer ou de faire glisser un caractère qui n’est pas en train de parler masque également automatiquement l’info-bulle, même si son paramètre Masquer automatiquement est désactivé. Vous pouvez modifier le paramètre de masquage automatique du caractère à l’aide de la propriété [**style**](style-property.md) de l’info-bulle.

### <a name="see-also"></a>Voir aussi

[**Propriété style**](style-property.md)


 

 





