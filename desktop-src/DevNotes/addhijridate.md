---
description: '\\Panneau de configuration HKCU \\ international.'
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: AddHijriDate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860809"
---
# <a name="addhijridate"></a>AddHijriDate

**\\Panneau de configuration HKCU \\ international**



| Type de données | Plage                      | Valeur par défaut |
|-----------|----------------------------|---------------|
| SZ de REG \_   | *Valeur d’ajustement valide* | (aucune)        |



 

## <a name="description"></a>Description

Spécifie des ajustements à la date dans le calendrier Hijri.

Le calendrier islamique est un calendrier lunaire utilisé dans le monde islamique. Les mois commencent et se terminent en fonction d’un décret basé sur l’observation de la nouvelle lune. Il est difficile de prédire avec précision les débuts et les fins des mois, et il existe des variations régionales, de sorte qu’un ajustement entre zéro et deux jours est apporté au calendrier.

La valeur de Registre **AddHijriDate** stocke cette valeur d’ajustement comme suit.



| Valeur          | Signification                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddHijriDate-2 | Soustraire deux jours.                                                                                                                                                                                                                    |
| AddHijriDate   | Soustraire un jour.                                                                                                                                                                                                                     |
| (vide)        | Aucun ajustement n’est nécessaire. (Si la date n’a pas été ajustée, cette entrée n’apparaît pas dans le registre. Si la date a été ajustée, puis restaurée à sa valeur d’origine, cette entrée apparaît dans le registre sans valeur.) |
| AddHijriDate + 1 | Ajoutez un jour.                                                                                                                                                                                                                          |
| AddHijriDate + 2 | Ajoutez deux jours.                                                                                                                                                                                                                         |



 

Par défaut, cette entrée n’existe pas dans le Registre. Vous pouvez l’ajouter à l’aide de l’éditeur du Registre Regedit.exe ou à l’aide de la méthode de modification décrite ci-dessous.

## <a name="change-method"></a>Modifier la méthode

Pour modifier la valeur de cette entrée ou l’ajouter au registre, commencez par installer les fichiers pour le script complexe et les langues de droite à gauche. Dans le panneau de configuration, cliquez sur **Options régionales et linguistiques**, puis cliquez sur l’onglet **langues** . Sous **prise en charge de langues supplémentaires**, activez la case à cocher pour **installer les fichiers de script complexe et les langues de droite à gauche (y compris le thaï)**. Cliquez sur **OK**.

Pour modifier la valeur de cette entrée, ou pour l’ajouter au registre, dans le panneau de configuration, cliquez sur **Options régionales et linguistiques**. Dans le champ **standards et formats** , sélectionnez les paramètres régionaux qui utilisent le calendrier Hijri. Cliquez sur le bouton **personnaliser** , puis sur l’onglet **Date** . Dans la liste déroulante **ajuster la date Hijri à :** , sélectionnez la valeur appropriée. Cliquez sur **OK**, puis de nouveau sur **OK** .

## <a name="activation-method"></a>Méthode d’activation

Les modifications apportées à cette entrée par le biais du panneau de configuration prennent effet immédiatement.

 

 



