---
description: Cette rubrique contient des informations de programmation. La liste suivante identifie des conseils de programmation pour vous aider à écrire un analyseur.
ms.assetid: 24d3e11f-8281-4464-a2d7-f4f2466e9d9e
title: Considérations relatives à la programmation (Moniteur réseau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2deb53a27d8abda4f45663b65fb922600a5b5386
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120224"
---
# <a name="programming-considerations-network-monitor"></a>Considérations relatives à la programmation (Moniteur réseau)

Cette rubrique contient des informations de programmation. La liste suivante identifie des conseils de programmation pour vous aider à écrire un analyseur.



| Conseil                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Installation automatique de votre analyseur                     | Implémentez la fonction [**ParserAutoInstallInfo**](parserautoinstallinfo.md) pour installer automatiquement votre analyseur et mettre à jour les fichiers ini associés. Si vous installez votre analyseur manuellement, vous devez mettre à jour tous les fichiers INI associés manuellement.                                                                                                                                                          |
| Analyse des propriétés de protocole                     | Implémentez la fonction [**AttachProperties**](attachproperties.md) pour analyser les propriétés de protocole. Évitez d’utiliser la fonction [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) quand vous attachez une instance de propriété et que vous l’utilisez uniquement pour des données non alignées sur un octet ou pour des données qui doivent être décodées. L’attachement de propriétés fait référence au mappage d’une instance de propriété à un emplacement spécifique dans une capture. |
| Analyse des protocoles répartis entre les frames | Supposons que chaque composant du Protocole se termine dans une trame et suppose que l’utilisateur appelle l’outil de fusion de protocole pour combiner les éléments dans un seul protocole. Ne cherchez pas dans un frame précédent lors de l’analyse d’un protocole et évitez d’essayer de reconstruire un protocole qui est fractionné entre les frames.                                                                                              |
| Mise en forme des données affichées                       | Appelez la fonction [**FormatPropertyInstance**](formatpropertyinstance.md) pour utiliser le formateur générique pour mettre en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau. Évitez d’écrire un formateur personnalisé pour les données d’affichage de l’interface utilisateur. Toutefois, vous pouvez appeler un formateur personnalisé pour créer une ligne de [*propriété de synthèse*](s.md) pour le protocole que vous analysez.            |
| Utilisation de CCAlloc                                   | Utilisez CCAlloc lorsque vous souhaitez Moniteur réseau allouer des données sur la base de la capture. Moniteur réseau ne spécifie pas l’ordre dans lequel les images appellent l’analyseur.                                                                                                                                                                                                                                                |
| Conservation de l’état d’un analyseur                      | Conserver l’état de l’opération de l’analyseur, car lorsque Moniteur réseau analyse une capture, il ne transmet pas les trames à l’analyseur dans un ordre spécifique. Pour cette raison, il est recommandé de ne pas conserver les données globales.                                                                                                                                                                                      |



 

 

 



