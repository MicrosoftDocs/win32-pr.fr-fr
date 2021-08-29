---
title: HelpFile, propriété
description: HelpFile, propriété
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0167034b064e8a6e7540dd22ff0b8185a8f96e82decf504aae4f4994b70d6694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478613"
---
# <a name="helpfile-property"></a>HelpFile, propriété

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

retourne ou définit le chemin d’accès et le nom de fichier d’un fichier d’aide contextuelle Microsoft Windows fourni par l’application cliente.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»)._ *  \[  =  *Nom de fichier* HelpFile\]



| Partie       | Description                                                                    |
|------------|--------------------------------------------------------------------------------|
| *Nom du fichier* | expression de chaîne spécifiant le chemin d’accès et le nom de fichier du fichier d’aide Windows. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété **HelpFile** du caractère, Agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **True** et que l’utilisateur clique sur le caractère ou sélectionne une commande dans son menu contextuel. Si vous avez spécifié un numéro de contexte dans la propriété [**HelpContextID**](helpcontextid-property.md) de la commande sélectionnée, help affiche une rubrique correspondant au contexte d’aide actuel. Sinon, elle affiche « aucune rubrique d’aide associée à cet élément ».

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**Propriété HelpModeOn**](helpmodeon-property.md), [ **HelpContextID, propriété**](helpcontextid-property.md)


 

 




