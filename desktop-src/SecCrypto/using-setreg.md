---
description: L’outil SetReg définit la valeur des clés de Registre qui contrôlent le comportement du processus de vérification du certificat Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Utilisation de SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114122"
---
# <a name="using-setreg"></a>Utilisation de SetReg

L’outil SetReg définit la valeur des clés de Registre qui contrôlent le comportement du processus de vérification du certificat Authenticode. Ces clés, appelées clés d’état de publication de logiciels, déterminent s’il faut approuver une racine de test, autoriser l’approbation hors connexion des certificats, tester les dates d’expiration des certificats et effectuer des vérifications de révocation.

La commande suivante répertorie la syntaxe et les options d’utilisation de SetReg.

**setreg- ?**

La commande suivante rend une racine de test approuvée. Par défaut, une racine de test n’est pas approuvée. Une fois les modifications apportées aux valeurs de clé effectuées, une liste de la valeur actuelle de toutes les valeurs de clé s’affiche. Si l’option **-q** est utilisée, les valeurs de clé ne sont pas affichées.

**setreg 1 TRUE**

La commande suivante rend une racine de test non fiable et entraîne la vérification de la révocation de toutes les vérifications. L’option **-q** est utilisée pour que la liste des valeurs de clés ne s’affiche pas

**setreg-q 1 faux 3 TRUE**

> [!Note]  
> Les commandes, les options et les arguments ne respectent pas la casse.

 

 

 



