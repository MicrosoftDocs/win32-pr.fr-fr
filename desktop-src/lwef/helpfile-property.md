---
title: HelpFile, propriété
description: HelpFile, propriété
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673481"
---
# <a name="helpfile-property"></a>HelpFile, propriété

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit le chemin d’accès et le nom de fichier d’un fichier d’aide contextuelle Microsoft Windows fourni par l’application cliente.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent. ***Caractères («*** CharacterID * * * »).* *  \[  =  *Nom de fichier* HelpFile\]



| Partie       | Description                                                                    |
|------------|--------------------------------------------------------------------------------|
| *Nom du fichier* | Expression de chaîne spécifiant le chemin d’accès et le nom de fichier du fichier d’aide Windows. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété **HelpFile** du caractère, agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur clique sur le caractère ou sélectionne une commande dans son menu contextuel. Si vous avez spécifié un numéro de contexte dans la propriété [**HelpContextID**](helpcontextid-property.md) de la commande sélectionnée, help affiche une rubrique correspondant au contexte d’aide actuel. Sinon, elle affiche « aucune rubrique d’aide associée à cet élément ».

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**Propriété HelpModeOn**](helpmodeon-property.md), [ **HelpContextID, propriété**](helpcontextid-property.md)


 

 




