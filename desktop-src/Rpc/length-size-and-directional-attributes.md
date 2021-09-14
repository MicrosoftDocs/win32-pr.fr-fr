---
title: Attributs de longueur, de taille et d’orientation
description: Lors du passage de tableaux entre le client et le serveur, les attributs liés à la taille \ Max \_ sont \ et \ size \_ est \ déterminer le nombre d’éléments de tableau que le stub serveur alloue.
ms.assetid: 2c95cf47-6fc0-4ccd-bb4f-acf356596e56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ffbf1ac75ad82a89e258ab595590fce2190b9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194131"
---
# <a name="length-size-and-directional-attributes"></a>Attributs de longueur, de taille et d’orientation

Lors du passage de tableaux entre le client et le serveur, les attributs liés à la taille \[ [**Max \_ sont**](/windows/desktop/Midl/max-is) \] et \[ [**size \_**](/windows/desktop/Midl/size-is) \] détermine le nombre d’éléments de tableau alloués par le stub serveur. La longueur des attributs liés à la longueur \[ [**\_ est**](/windows/desktop/Midl/length-is) \] , \[ en [**premier lieu \_**](/windows/desktop/Midl/first-is) \] , et le \[ [**dernier \_**](/windows/desktop/Midl/last-is) \] détermine le nombre d’éléments transmis au serveur et au client.

Différents attributs directionnels peuvent être appliqués aux paramètres. Toutefois, certaines combinaisons d’attributs directionnels peuvent provoquer des erreurs. Par exemple, supposez que vous écrivez une interface qui spécifie une procédure avec deux paramètres, un tableau et la longueur transmise du tableau. Le terme « *dir \_ attr* » fait référence à l’attribut directionnel appliqué au paramètre comme suit :

``` syntax
Proc1(
    [dir_attr] short *plength;
    [dir_attr, length_is(pLength)] short array[MAX_SIZE]);
```

Le comportement du compilateur MIDL pour chaque combinaison d’attributs directionnels est décrit dans le tableau suivant.



| Array                                          | Paramètre de longueur                               | Actions stub lors de l’appel du client au serveur                                                                                                                                                                                                                          | Actions stub au retour du serveur au client                                                                                                                                                                         |
|------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[**dans**](/windows/desktop/Midl/in)\]                          | \[[**dans**](/windows/desktop/Midl/in)\]                          | Transmettez la longueur et le nombre d’éléments indiqués par le paramètre.                                                                                                                                                                                              | Aucune donnée n’est transmise.                                                                                                                                                                                                 |
| \[[**dans**](/windows/desktop/Midl/in)\]                          | \[[**à**](/windows/desktop/Midl/out-idl)\]                    | Non légal ; Erreur du compilateur MIDL.                                                                                                                                                                                                                                         | Non légal ; Erreur du compilateur MIDL.                                                                                                                                                                                      |
| \[[**dans**](/windows/desktop/Midl/in)\]                          | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmettez la longueur et le nombre d’éléments indiqués par le paramètre de longueur.                                                                                                                                                                                       | Transmet uniquement la longueur.                                                                                                                                                                                            |
| \[[**à**](/windows/desktop/Midl/out-idl)\]                    | \[[**dans**](/windows/desktop/Midl/in)\]                          | Transmettez la longueur.<br/> Si la taille du tableau est fixe, allouez la taille du tableau sur le serveur, mais ne transmettez pas d’éléments.<br/> Si la taille du tableau n’est pas liée, non conforme : erreur du compilateur MIDL.<br/>                                                              | Transmet le nombre d’éléments indiqué par la longueur.<br/> Notez que la longueur peut être modifiée et peut avoir une valeur différente de la valeur sur le client. Ne transmettez pas la longueur.<br/>          |
| \[[**à**](/windows/desktop/Midl/out-idl)\]                    | \[[**à**](/windows/desktop/Midl/out-idl)\]                    | Allouez de l’espace pour le paramètre de longueur sur le serveur, mais ne transmettez pas le paramètre. Si la taille du tableau est fixe, allouez la taille du tableau sur le serveur, mais ne transmettez pas d’éléments.<br/> Si la taille du tableau n’est pas fixe, non conforme : erreur du compilateur MIDL.<br/> | Transmettez la longueur et le nombre d’éléments indiqués par la longueur telle qu’elle est définie par l’application serveur.                                                                                                             |
| \[[**à**](/windows/desktop/Midl/out-idl)\]                    | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmettez le paramètre de longueur. Si la taille du tableau est liée, allouez la taille du tableau sur le serveur, mais ne transmettez pas d’éléments.<br/> Si la taille du tableau n’est pas liée, non conforme : erreur du compilateur MIDL.<br/>                                                           | Transmettez la longueur. Transmet le nombre d’éléments de tableau indiqué par la longueur.<br/>                                                                                                                       |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**dans**](/windows/desktop/Midl/in)\]                          | Transmettez la longueur et le nombre d’éléments indiqués par le paramètre.                                                                                                                                                                                              | Ne transmettez pas la longueur. Transmet le nombre d’éléments indiqué par la longueur.<br/> Notez que la longueur peut être modifiée et peut avoir une valeur différente de la valeur d’origine sur le client.<br/> |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**à**](/windows/desktop/Midl/out-idl)\]                    | Non légal ; Erreur du compilateur MIDL.                                                                                                                                                                                                                                         | Non légal ; Erreur du compilateur MIDL.                                                                                                                                                                                      |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Transmettez la longueur et le nombre d’éléments indiqués par le paramètre.                                                                                                                                                                                              | Transmettez la longueur et le nombre d’éléments indiqués par le paramètre.                                                                                                                                           |



 

En général, vous ne devez pas modifier les paramètres de longueur ou de taille côté serveur. Si vous modifiez le paramètre de longueur, vous pouvez disposer de mémoire orpheline. Pour plus d’informations, consultez [orphelins de mémoire](memory-orphaning.md).

 

