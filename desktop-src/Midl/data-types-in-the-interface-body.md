---
title: Types de données dans le corps de l’interface
description: Le corps de l’interface, qui est placé entre accolades (), contient les types de données qui seront utilisés dans les appels de procédure distante et les prototypes pour les fonctions qui seront exécutées à distance.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- interfaces MIDL, types de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6691ccf89e1bff3b0e980678a30c6f706b724e4f30192d7960183c00cc00c237
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979708"
---
# <a name="data-types-in-the-interface-body"></a>Types de données dans le corps de l’interface

Le corps de l’interface, qui est placé entre accolades ({}), contient les types de données qui seront utilisés dans les appels de procédure distante et les prototypes pour les fonctions qui seront exécutées à distance. Un corps d’interface peut contenir des importations, des pragmas, des déclarations de constantes, des déclarations de type et des déclarations de fonction. Sauf en mode de compatibilité OSF, le compilateur MIDL autorise également les déclarations implicites sous la forme de définitions de variables.

Notez que la spécification OSF-DCE pour les interfaces RPC n’autorise pas plusieurs interfaces dans un seul fichier IDL. Par conséquent, si vous compilez en mode de compatibilité OSF ( [**/OSF**](-osf.md)) MIDL, votre fichier IDL ne peut contenir qu’une seule interface.

Pour plus d’informations sur l’utilisation du compilateur MIDL pour produire des bibliothèques de types, consultez [génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md).

Dans Microsoft RPC, un fichier IDL peut contenir plusieurs interfaces et ces interfaces peuvent être transmises par progression déclarées (dans le fichier IDL qui les définit). Par exemple :

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




