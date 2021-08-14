---
title: Attributs de champ
description: Attributs de champ (attributs appliqués aux champs d’un tableau, d’une structure, d’une Union ou d’un tableau de caractères) et appel de procédure distante (RPC).
ms.assetid: 4508479d-ff0a-4698-94aa-588837032067
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6d14bab0cf14710e91fceb466111c4af32d3d2828e4b7bdacc9494fa27b7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929998"
---
# <a name="field-attributes"></a>Attributs de champ

Les attributs de champ sont les attributs qui peuvent être appliqués aux champs d’un tableau, d’une structure, d’une Union ou d’un tableau de caractères :

-   **\[**[**Ignorer**](/windows/desktop/Midl/ignore) **\]** , la **\[** [ **taille \_ est**](/windows/desktop/Midl/size-is)**\]**
-   **\[**[**le nombre maximal \_ est**](/windows/desktop/Midl/max-is)**\]**
-   **\[**[**la longueur \_ est**](/windows/desktop/Midl/length-is)**\]**
-   **\[**[**tout d’abord, \_**](/windows/desktop/Midl/first-is)**\]**
-   **\[**[**la dernière \_ est**](/windows/desktop/Midl/last-is)**\]**
-   **\[**[**le commutateur \_ est**](/windows/desktop/Midl/switch-is)**\]**
-   **\[**[**chaîne**](/windows/desktop/Midl/string)**\]**
-   [attributs de pointeur](three-pointer-types.md)

Par exemple, les attributs de champ sont utilisés conjointement avec les déclarations de tableau pour spécifier la taille du tableau ou la partie du tableau qui contient des données valides. Pour ce faire, vous associez un autre paramètre, un champ de structure ou une expression constante au tableau.

L' **\[** attribut [**ignore**](/windows/desktop/Midl/ignore) **\]** désigne les champs de pointeur à ignorer pendant le processus de marshaling. Un tel champ ignoré a la valeur **null** côté récepteur.

MIDL fournit des tableaux *conformes*, *variables* et *ouverts* . Un tableau est appelé conforme si ses limites sont déterminées au moment de l’exécution. La **\[** [**taille \_ est**](/windows/desktop/Midl/size-is) l' **\]** attribut désignant la limite supérieure de la taille d’allocation du tableau et l' **\[** attribut [**Max \_ is**](/windows/desktop/Midl/max-is) **\]** désigne la limite supérieure de la valeur d’un index de tableau valide. Pour plus d’informations, consultez **\[** [**tableaux**](arrays.md) **\]** .

Un tableau est appelé varying si ses limites sont déterminées au moment de la compilation, mais la plage d’éléments transmis est déterminée au moment de l’exécution. Un tableau ouvert (également appelé tableau variable conforme) est un tableau dont la limite supérieure et la plage d’éléments transmis sont déterminées au moment de l’exécution. Pour déterminer la plage d’éléments transmis d’un tableau, la déclaration de tableau doit inclure une **\[** [**longueur \_**](/windows/desktop/Midl/length-is) **\]** , **\[** [**First \_ is**](/windows/desktop/Midl/first-is) **\]** ou **\[** [**Last \_ is**](/windows/desktop/Midl/last-is) **\]** attribute.

La **\[ longueur \_ est \]** l’attribut désignant le nombre d’éléments de tableau à transmettre et le **\[ premier attribut \_ est \]** désignant l’index du premier élément de tableau à transmettre. Le **\[ dernier \_ attribut \] est** désignant l’index du dernier élément de tableau à transmettre.

Le **\[** [**commutateur \_ est**](/windows/desktop/Midl/switch-is) **\]** un attribut de champ qui désigne un discriminateur d’Union. Lorsque l’Union est un paramètre de procédure, le discriminateur d’Union doit être un autre paramètre de la même procédure. Lorsque l’Union est un champ d’une structure, le discriminateur doit être un autre champ de la structure au même niveau que le champ Union. Le discriminateur doit être un type [**booléen**](/windows/desktop/Midl/boolean), [**char**](/windows/desktop/Midl/char-idl), [**int**](/windows/desktop/Midl/int)ou [**enum**](/windows/desktop/Midl/enum) , ou un type qui correspond à l’un de ces types. Pour plus d’informations, consultez Unions **\[ \_ non \]** [encapsulées](/windows/desktop/Midl/nonencapsulated-unions) et commutateur.

L' **\[** attribut de champ de [**chaîne**](/windows/desktop/Midl/string) **\]** désigne qu’un caractère unidimensionnel ou un tableau d’octets, ou un pointeur vers un flux de caractères ou d’octets se terminant par zéro, doit être traité comme une chaîne. L’attribut de chaîne s’applique uniquement aux tableaux et pointeurs unidimensionnels. Le type d’élément est limité à [**char**](/windows/desktop/Midl/char-idl), [**Byte**](/windows/desktop/Midl/byte), [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t)ou à un type nommé qui correspond à l’un de ces types.

Pour plus d’informations sur le contexte dans lequel les attributs de champ s’affichent, consultez [tableaux MIDL](/windows/desktop/Midl/midl-arrays), [structures MIDL](/windows/desktop/Midl/midl-structures)et [unions MIDL](/windows/desktop/Midl/midl-unions).

 

 