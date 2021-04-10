---
description: Le BIOS virtuel est une image logicielle qui est chargée dans la mémoire RAM pour configurer certains des aspects de base de et démarrer un système informatique. Il y a un seul élément BIOS par système informatique et cet élément ne peut pas être remplacé ou supprimé.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Classes BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952052"
---
# <a name="bios-classes"></a>Classes BIOS

Le BIOS virtuel est une image logicielle qui est chargée dans la mémoire RAM pour configurer certains des aspects de base de et démarrer un système informatique. Il y a un seul élément BIOS par système informatique et cet élément ne peut pas être remplacé ou supprimé. Par conséquent, il n’existe pas de pool de ressources pour l’ajout de nouveaux éléments BIOS à la machine virtuelle. L’élément BIOS n’a pas non plus sa propre classe SettingData pour décrire les paramètres du BIOS. Les paramètres du BIOS, tels que les numéros de série, l’ordre de démarrage et l’état VERR. num, se trouvent dans la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .

Voici les classes WMI de virtualisation associées au BIOS. Ces classes se trouvent dans le \\ \\ . \\ \\Espace de noms de virtualisation racine.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                    | Description                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**MSVM \_ BIOSElement**](msvm-bioselement.md)<br/> | Représente le logiciel de bas niveau qui est chargé dans la mémoire RAM pour configurer et démarrer le système.<br/> |
| [**MSVM \_ SystemBIOS**](msvm-systembios.md)<br/>   | Utilisé pour associer un ordinateur virtuel à son BIOS.<br/>                                           |



 

 

 




