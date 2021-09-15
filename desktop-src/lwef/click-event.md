---
title: Événement clic
description: Événement clic
ms.assetid: 772029d5-97b6-49d8-a989-04f0fc429aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3956d19e833a3e0a5f71192b2846ef9cb270ad10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518428"
---
# <a name="click-event"></a>Événement clic

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque l’utilisateur clique sur un caractère ou sur l’icône du caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sous-** *agent * * * \_ Click* *  **(ByVal** *CharacterID*, *bouton* **ByVal** , **ByVal** *MAJ*, **ByVal** *X*, **ByVal** *Y * * *)**



| Partie          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère sur lequel l’utilisateur a cliqué sous forme de chaîne.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Button*      | Retourne un entier qui identifie le bouton qui a été enfoncé et relâché pour déclencher l’événement. L’argument Button est un champ de bits avec les bits correspondant au bouton gauche (bit 0), le bouton droit (bit 1) et le bouton central (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. Seul l’un des bits est défini, ce qui indique le bouton à l’origine de l’événement. Si le caractère comprend une icône de barre des tâches et que le bit 13 est également défini, le clic s’est produit sur l’icône de la barre des tâches.                                                                                                                                                                      |
| *Majuscule*       | Retourne un entier qui correspond à l’état des touches Maj, CTRL et ALT lorsque le bouton spécifié dans l’argument de bouton est enfoncé ou relâché. Un bit est défini si la touche est enfoncée. L’argument Shift est un champ de bits avec les bits de poids faible correspondant à la touche Maj (bit 0), la touche CTRL (bit 1) et la touche ALT (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. L’argument Shift indique l’état de ces clés. Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée. Par exemple, si les touches CTRL et ALT étaient enfoncées, la valeur de Shift serait 6. |
| *X, Y*         | Retourne un entier qui spécifie l’emplacement actuel du pointeur de la souris. Les valeurs X et Y sont toujours exprimées en pixels, par rapport à l’angle supérieur gauche de l’écran.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Remarques

Cet événement est envoyé uniquement au client d’entrée-actif d’un caractère. Lorsque l’utilisateur clique sur un caractère ou sur son icône de barre des tâches sans client d’entrée-actif, le serveur envoie l’événement à son client actif. Si le caractère est [**visible (**](visible-property.md)  =  **true**), l’action de l’utilisateur définit également le dernier client d’entrée-actif du caractère en tant que client d’entrée-actif en cours, en envoyant l’événement [**ActivateInput**](activateinput-event.md) à ce client, puis en envoyant l’événement **Click** . Si le caractère est masqué (  =  **false** visible) et que l’utilisateur clique sur l’icône de barre des tâches du caractère en utilisant le bouton 1, le caractère s’affiche également automatiquement.

> [!Note]  
> Le fait de cliquer sur un caractère ne désactive pas toutes les autres sorties de caractères (tous les caractères). Toutefois, le fait d’appuyer sur la touche d’écoute vide la sortie du caractère d’entrée-actif et déclenche l’événement [**RequestComplete**](requestcomplete-event.md) , en passant une [requête. Status](status-property.md) qui indique que la file d’attente du client a été interrompue.

 

 

 




