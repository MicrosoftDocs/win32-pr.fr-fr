---
title: Événement de commande
description: Événement de commande
ms.assetid: 3e180286-dfa0-4b34-90ee-3267ed6f48af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5647e7eac3aaba0a6094be6b52cc3726eba34ad7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031209"
---
# <a name="command-event"></a>Événement de commande

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque l’utilisateur choisit une commande (du client).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Commande Sub** *agent* \_  **(ByVal** *UserInput * * *)**



| Partie        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *UserInput* | Identifie l’objet de [**commande**](/windows/desktop/lwef/the-command-object) retourné par le serveur. <br/> Vous pouvez accéder aux propriétés suivantes à partir de l’objet de [**commande**](/windows/desktop/lwef/the-command-object) :<br/> CharacterID <br/> Valeur de chaîne identifiant le nom (ID) du caractère qui a reçu la commande. <br/> [**Nom**](name-property.md)<br/> Valeur de chaîne identifiant le nom (ID) de la commande.<br/> [**Garantir**](confidence-property.md)<br/> Valeur entière de type long indiquant le score de confiance de la commande. <br/> [**Voix**](voice-property.md) <br/> Valeur de chaîne identifiant le texte vocal de la commande.<br/> Alt1Name <br/> Valeur de chaîne identifiant le nom de la prochaine commande (deuxième) Best.<br/> Alt1Confidence <br/> Valeur entière de type long indiquant le score de confiance de la prochaine commande (deuxième) Best.<br/> Alt1Voice <br/> Valeur de chaîne identifiant le texte vocal pour la meilleure correspondance de commande suivante.<br/> Alt2Name <br/> Valeur de chaîne identifiant le nom de la troisième meilleure correspondance de commande.<br/> Alt2Confidence <br/> Entier long identifiant le score de confiance pour la troisième meilleure correspondance de commande.<br/> Alt2Voice <br/> Valeur de chaîne identifiant le texte vocal pour la troisième meilleure correspondance de commande.<br/> [**Saut**](count-property.md) <br/> Valeur entière de type long indiquant le nombre d’alternatives retournées.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Le serveur vous avertit de cet événement lorsque votre application est en entrée-active et que l’utilisateur choisit une commande en entrant oral ou le menu contextuel d’un caractère. L’événement renvoie le nombre de commandes correspondantes possibles dans [**Count**](count-property.md) , ainsi que le nom, le score de confiance et le texte vocal de ces correspondances.

Si l’entrée vocale déclenche cet événement, le serveur retourne une chaîne qui identifie la meilleure correspondance dans le paramètre de [**nom**](name-property.md) , et la deuxième et la troisième correspondance dans Alt1Name et Alt2Name. Une chaîne vide indique que l’entrée ne correspond à aucune commande définie par votre application. par exemple, il peut s’agir de l’une des commandes définies par le serveur. Si la commande a été mise en correspondance avec la commande de l’agent ; par exemple, Hide, une chaîne vide est retournée dans le paramètre **Name** , mais vous continuez à recevoir le texte entendu dans le paramètre [**Voice**](voice-property.md) .

Vous pouvez obtenir le même nom de commande retourné dans plusieurs entrées. Les paramètres [**confidence**](confidence-property.md), Alt1Confidence et Alt2Confidence retournent les scores relatifs, dans la plage comprise entre-100 et 100, retournés par le moteur de reconnaissance vocale pour chaque correspondance respective. Les paramètres [**Voice**](voice-property.md), Alt1Voice et Alt2Voice retournent le texte vocal que le moteur de reconnaissance vocale a mis en correspondance pour chaque alternative. Si [**Count**](count-property.md) retourne la valeur zéro (0), le serveur a détecté une entrée parlée, mais a déterminé qu’il n’y avait pas de commande correspondante.

Si l’entrée vocale n’est pas la source de la commande, par exemple si l’utilisateur a sélectionné la commande dans le menu contextuel du caractère, le serveur renvoie le nom (ID) de la commande sélectionnée dans la propriété [**nom**](name-property.md). Elle retourne également la valeur du paramètre [**confidence**](confidence-property.md) comme 100 et la valeur des paramètres [**vocaux**](voice-property.md) comme chaîne vide (""). Alt1Name et Alt2Name retournent également des chaînes vides. Alt1Confidence et Alt2Confidence retournent zéro (0), et Alt1Voice et Alt2Voice retournent des chaînes vides. [**Count**](count-property.md) retourne 1.

> [!Note]  
> Tous les moteurs de reconnaissance vocale ne peuvent pas retourner toutes les valeurs de tous les paramètres de cet événement. Contactez votre fournisseur de moteur pour déterminer si le moteur prend en charge l’interface de l’API Microsoft Speech pour retourner des alternatives et des scores de confiance.

 

 

