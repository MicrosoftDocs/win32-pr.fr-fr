---
title: Règles de conception d’interface
description: Cette section fournit un bref résumé des règles et des instructions de conception d’interface.
ms.assetid: c43fc385-bcd6-45fc-91b2-ad9827fdb15c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c1cde73527ac79a2e4442910e3053ed96748337
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102384"
---
# <a name="interface-design-rules"></a>Règles de conception d’interface

Cette section fournit un bref résumé des règles et des instructions de conception d’interface. Certaines de ces règles sont spécifiques à l’architecture COM, tandis que d’autres sont des restrictions imposées par le langage de conception d’interface, MIDL. Pour plus d’informations sur la conception de l’interface COM, consultez [anatomie d’un fichier IDL](anatomy-of-an-idl-file.md).

Par définition, un objet n’est pas un objet COM, sauf s’il implémente l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) ou une interface dérivée de **IUnknown**. En outre, les règles suivantes s’appliquent à toutes les interfaces implémentées sur un objet COM :

-   Ils doivent avoir un identificateur d’interface (IID) unique.
-   Ils doivent être immuables. Une fois qu’elles ont été créées et publiées, aucune partie de leur définition ne peut changer.
-   Toutes les méthodes d’interface doivent retourner une valeur **HRESULT** afin que les parties du système qui gèrent le traitement à distance puissent signaler des erreurs RPC.
-   Tous les paramètres de chaîne dans les méthodes d’interface doivent être au format Unicode.
-   Vos types de données doivent être accessibles à distance. Si vous ne pouvez pas convertir un type de données en un type accessible à distance, vous devrez créer vos propres routines de marshaling et de démarshaling. En outre, **LPVOID**, **ou \* void**, n’a aucune signification sur un ordinateur distant. Utilisez un pointeur vers [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), si nécessaire.

> [!Note]  
> L’implémentation actuelle de MIDL ne gère pas la surcharge de fonction ou l’héritage multiple.

 

## <a name="other-interface-design-considerations"></a>Autres considérations relatives à la conception d’interface

Utilisez des pointeurs vers des données très soigneusement. Pour recréer les données dans l’espace d’adressage du processus appelé, le temps d’exécution RPC doit connaître la taille exacte des données. Si, par exemple, un **paramètre \* char** pointe vers une mémoire tampon de caractères plutôt qu’un caractère unique, les données ne peuvent pas être recréées correctement. Utilisez la syntaxe disponible avec MIDL pour décrire avec précision les structures de données représentées par vos définitions de type.

L’initialisation est essentielle pour les pointeurs qui sont incorporés dans les tableaux et les structures et passés au-delà des limites du processus. Les pointeurs non initialisés peuvent fonctionner lorsqu’ils sont passés à un programme dans le même espace de processus, mais les proxies et les stubs partent du principe que tous les pointeurs sont initialisés avec des adresses valides ou qu’ils ont la valeur null.

Soyez prudent lors de l’alias des pointeurs (permettant aux pointeurs de pointer vers la même mémoire). Si l’alias est intentionnel, ces pointeurs doivent être déclarés avec un alias dans le fichier IDL. Les pointeurs déclarés comme sans alias ne doivent jamais s’alias mutuellement.

Soyez attentif à la façon dont vous allouez et libérez de la mémoire. N’oubliez pas que, sauf si vous indiquez explicitement à un objet COM (à l’aide de l’attribut [**allocate**](/windows/desktop/Midl/allocate) ) de ne pas libérer une structure de données qui a été créée pendant un appel hors processus, cette structure sera détruite à la fin de l’appel. Envisagez également la surcharge potentiellement destructrice créée par une allocation inefficace des structures de données qui doivent désormais être marshalées et démarshalées.

Enfin, soyez prudent lors de la définition de vos valeurs de retour **HRESULT** afin de ne pas créer de codes d’erreur qui sont en conflit avec les codes ITF de l’infrastructure définie par com \_ (les valeurs entre 0x0000 et 0x01FF sont réservées) ou qui sont en conflit avec d’autres valeurs **HRESULT** ayant la même valeur. Dans la mesure du possible, utilisez les valeurs de retour de réussite et d’échec de COM universel, et utilisez un paramètre [**out**](/windows/desktop/Midl/out-idl) plutôt qu’un **HRESULT** pour retourner des informations spécifiques à l’appel de fonction.

Pour plus d'informations, voir les rubriques suivantes :

-   [Conception d’interfaces accessibles à distance](designing-remotable-interfaces.md)
-   [Utilisation d’une interface COM](using-a-com-interface.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définitions d’interface et bibliothèques de types](/windows/desktop/Midl/interface-definitions-and-type-libraries)
</dt> </dl>

 

 