---
description: Le BIOS virtuel est une image logicielle qui est chargée dans la mémoire RAM pour configurer certains des aspects de base de et démarrer un système informatique. Il y a un seul élément BIOS par système informatique et cet élément ne peut pas être remplacé ou supprimé.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Classes BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9605f28a23fc84b653ba5efe6c6e4be057eba48da81ddb777c7516d1317da6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813636"
---
# <a name="bios-classes"></a>Classes BIOS

Le BIOS virtuel est une image logicielle qui est chargée dans la mémoire RAM pour configurer certains des aspects de base de et démarrer un système informatique. Il y a un seul élément BIOS par système informatique et cet élément ne peut pas être remplacé ou supprimé. Par conséquent, il n’existe pas de pool de ressources pour l’ajout de nouveaux éléments BIOS à la machine virtuelle. L’élément BIOS n’a pas non plus sa propre classe SettingData pour décrire les paramètres du BIOS. Paramètres pour le BIOS, telles que les numéros de série, l’ordre de démarrage et l’état de verr. num, se trouvent dans la classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .

Voici les classes WMI de virtualisation associées au BIOS. Ces classes se trouvent dans le \\ \\ . \\ \\Espace de noms de virtualisation racine.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                    | Description                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**MSVM \_ BIOSElement**](msvm-bioselement.md)<br/> | Représente le logiciel de bas niveau qui est chargé dans la mémoire RAM pour configurer et démarrer le système.<br/> |
| [**MSVM \_ SystemBIOS**](msvm-systembios.md)<br/>   | Utilisé pour associer un ordinateur virtuel à son BIOS.<br/>                                           |



 

 

 




