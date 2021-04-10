---
description: Pour envoyer des données sur un support de communication comme une ligne téléphonique, les données doivent être sérialisées&\# 8212 ; autrement dit, elles sont converties en une chaîne de uns et de zéros transmises en série sur la ligne.
ms.assetid: ef8982dc-bbbc-466a-9afe-dd0425c23f1d
title: Données encodées et décodées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b130232ac67503c6a20835c4c9b4e728b36f8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951084"
---
# <a name="encoded-and-decoded-data"></a>Données encodées et décodées

Pour envoyer des données sur un support de communication tel qu’une ligne téléphonique, les données doivent être [*sérialisées*](../secgloss/s-gly.md), c’est-à-dire converties en une chaîne de uns et de zéros transmis en série sur la ligne. La sérialisation doit être effectuée de manière à ce que l’ordinateur qui reçoit les données puisse reconvertir les données dans leur format d’origine. La façon dont la sérialisation est accomplie est appelée [*protocole de communication*](../secgloss/c-gly.md)et est contrôlée par le matériel de transmission de données et de logiciel. Il existe plusieurs niveaux à partir desquels les données sont converties. L’illustration suivante montre une vue beaucoup simplifiée des couches de protocole de communication.

![couches de protocole de communication](images/layer.png)

L’illustration précédente montre la couche d’application sur l’ordinateur \# 1 qui envoie les données à transmettre (qui se compose généralement d’une combinaison de caractères et de chiffres textuels) vers la couche de codage/décodage. La couche de codage/décodage encode les données en un flux d’octets ordinateur. Au niveau le plus bas, la couche matérielle, le matériel convertit les octets de données en un flux série de uns et de zéros transmis sur la ligne à l’ordinateur \# 2. La couche matérielle de l’ordinateur \# 2 convertit les zéros et les zéros en octets de l’ordinateur, puis les transmet à la couche de codage/décodage pour le décodage. La couche de codage/décodage décode les octets dans leur format d’origine et transmet les données jusqu’à la couche application.

Un principe de conception de logiciels accepté consiste à utiliser l' *abstraction*, c’est-à-dire le processus de description d’un problème ou d’un objet en termes de paramètres généraux plutôt que de décrire tous les détails nécessaires pour résoudre le problème, ou de décrire tous les détails d’un objet. À l’aide de l’abstraction, un concepteur peut spécifier un objet logiciel qui a des qualités spécifiques sans se soucier de la façon dont l’objet est réellement implémenté dans le code logiciel. Une telle pratique laisse l’implémentation ouverte. Elle simplifie également la spécification et permet d’indiquer les Axioms sur l’objet qui peuvent être prouvés lorsque l’objet est implémenté. Ces Axioms peuvent ensuite être utilisés lorsque l’objet est utilisé dans un autre objet de niveau supérieur. L’abstraction est la caractéristique de la plupart des spécifications logicielles contemporaines.

La plupart des [*protocoles de communication*](../secgloss/c-gly.md) impliquent une bonne abstraction. Les objets à des couches supérieures sont définis de façon abstraite et sont destinés à être implémentés à l’aide d’objets aux couches inférieures. Par exemple, un service sur une couche peut nécessiter le transfert de certains objets abstraits entre les ordinateurs. Une couche de niveau inférieur peut utiliser des règles de codage pour transformer les objets abstraits en chaînes de uns et de zéros.

Une méthode courante de spécification d’objets abstraits destinés à être transmis en série est appelée ASN. 1 ( [*Abstract Syntax Notation One*](../secgloss/a-gly.md) ). ASN. 1 est défini dans la recommandation CCITT [*X. 208*](../secgloss/x-gly.md). Un ensemble de règles ASN. 1 pour représenter des objets de ce type en tant que chaînes de uns et de zéros est appelé le [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) et est défini dans la recommandation CCITT [*X. 509*](../secgloss/x-gly.md), section 8,7. Il s’agit des méthodes d’encodage actuellement utilisées par CryptoAPI.

Pour plus d’informations sur les fonctions encoder/décoder, consultez [fonctions d’encodage et de décodage d’objets](cryptography-functions.md).

 

 
