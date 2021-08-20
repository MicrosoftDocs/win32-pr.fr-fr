---
title: Génération d’UUID d’interface
description: Génération d’identificateurs uniques universels (UUID) d’interface et utilisation de uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c21ead6161a79d000d2741a49c4fb61ff23b3a8a3340db2eb26a7805424df5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929546"
---
# <a name="generating-interface-uuids"></a>Génération d’UUID d’interface

Cette section fournit des informations sur les identificateurs uniques universels (UUID) et l’utilitaire uuidgen dans les rubriques suivantes :

-   [Qu’est-ce qu’un UUID ?](#what-is-a-uuid)
-   [Utilisation de uuidgen](#using-uuidgen)

## <a name="what-is-a-uuid"></a>Qu’est-ce qu’un UUID ?

Toutes les interfaces doivent être identifiées de manière unique sur un réseau afin que les clients puissent les trouver. Sur les réseaux de petite taille, le nom de l’interface seul peut suffire pour l’identifier. Toutefois, cela n’est généralement pas possible sur les réseaux de grande taille. Par conséquent, les développeurs attribuent généralement un identificateur unique universel (UUID, interchangeable avec le terme GUID ou un identificateur global unique) à chaque interface. Un UUID est une chaîne qui contient un jeu de chiffres hexadécimaux. Chaque interface possède un UUID différent. Pour plus d’informations, consultez [UUID de chaîne](string-uuid.md).

La représentation textuelle d’un UUID est une chaîne composée de 8 chiffres hexadécimaux suivis d’un trait d’Union, suivi de trois groupes séparés par des tirets de 4 chiffres hexadécimaux, suivis d’un trait d’Union, suivi de 12 chiffres hexadécimaux. L’exemple suivant est une chaîne UUID valide :

ba209999-0c6c-11d2-97cf-00c04f8eea45

Les UUID vides sont appelés UUID nuls et non **null** . Le terme « Nil » indique tout ce qui est zéro, vide, vide ou non initialisé. Une chaîne vide, un enregistrement de base de données vide ou un UUID non initialisé sont des exemples de valeurs Nil.

> [!Note]  
> La valeur **null** correspond à la valeur zéro spécifique. Il est souvent utilisé dans la programmation C et C++ conjointement avec les pointeurs. Nil est un terme plus général que **null**. Les UUID non initialisés de l’interface d’objet doivent toujours être appelés UUID NULL plutôt que des UUID **null** .

 

## <a name="using-uuidgen"></a>Utilisation de uuidgen

Microsoft fournit un programme utilitaire appelé uuidgen pour générer vos UUID. L’utilitaire uuidgen génère l’UUID au format de fichier IDL ou au format de langage C.

Quand vous exécutez l’utilitaire uuidgen à partir de la ligne de commande, vous pouvez utiliser les commutateurs de commande suivants.



| Commutateur uuidgen           | Description                                                                |
|--------------------------|----------------------------------------------------------------------------|
| **/I**                   | Génère l’UUID dans un modèle d’interface IDL.                                 |
| **commutateur**                   | Génère l’UUID en tant que structure C initialisée.                                |
| **/o** < *nom du fichier*> | Redirige la sortie vers un fichier ; spécifié immédiatement après le commutateur **/o** . |
| **/n** < *nombre*>   | Spécifie le nombre d’UUID à générer.                                 |
| **/v**                   | Affiche des informations de version sur uuidgen.                                |
| **/h** ou **?**          | Affiche le résumé des options de commande.                                           |



 

En général, vous allez utiliser l’utilitaire uuidgen comme indiqué dans l’exemple suivant.

**uuidgen-i-oMyApp. idl**

Cette commande génère un UUID et le stocke dans un fichier MIDL que vous pouvez utiliser comme modèle. Lorsque la commande précédente est exécutée, le contenu de MyApp. idl est semblable à ce qui suit :

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

L’étape suivante consiste à remplacer le nom de l’espace réservé, NOMINTERFACE, par le nom réel de votre interface.

 

 




