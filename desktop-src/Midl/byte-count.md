---
title: attribut byte_count
description: L’attribut \ \_ CCP Count \ ACF est un attribut de paramètre qui associe une taille, en octets, à la zone de mémoire indiquée par le pointeur.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count MIDL de l’attribut
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093757"
---
# <a name="byte_count-attribute"></a>attribut de nombre d’octets \_

L’attribut ACF de **\[ \_ nombre \] d’octets** est un attribut de paramètre qui associe une taille, en octets, à la zone de mémoire indiquée par le pointeur.

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*function-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs de fonction ACF.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction définie dans le fichier IDL. Le nom de la fonction est obligatoire.

</dd> <dt>

*Length-variable-name* 
</dt> <dd>

Spécifie le nom du paramètre [**\[ en \]**](in.md)uniquement qui spécifie la taille, en octets, de la zone mémoire référencée par le *paramètre-Name*.

</dd> <dt>

*nom du paramètre* 
</dt> <dd>

Spécifie le nom du paramètre de pointeur en [**\[ sortie \]**](out-idl.md)seule défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

Le **\[ \_ nombre \] d’octets** de l’attribut ACF représente une extension Microsoft de l’IDL DCE. Par conséquent, cet attribut n’est pas disponible lorsque vous utilisez le commutateur du compilateur MIDL [**/OSF**](-osf.md).

> [!Note]  
> L’attribut **\[ nombre \] d’octets** n’est plus pris en charge dans la syntaxe NDR64 en raison de la difficulté à estimer la taille requise pour tous les paramètres de [**\[ sortie \]**](out-idl.md) .

 

La mémoire référencée par le paramètre de pointeur est contiguë et n’est pas allouée ou libérée par les stubs client. Cette fonctionnalité de l’attribut **\[ \_ nombre \] d’octets** vous permet de créer une zone de mémoire tampon persistante dans la mémoire du client qui peut être réutilisée lors de plusieurs appels à la procédure distante.

La possibilité de désactiver l’allocation de mémoire stub du client vous permet de régler l’efficacité de l’application. Par exemple, l’attribut **\[ \_ nombre \] d’octets** peut être utilisé par les fonctions de fournisseur de service qui utilisent Microsoft RPC. Lorsqu’une application utilisateur appelle l’API du fournisseur de services et envoie un pointeur vers une mémoire tampon, le fournisseur de services peut passer le pointeur de la mémoire tampon à la fonction distante. Le fournisseur de services peut réutiliser la mémoire tampon pendant plusieurs appels distants sans forcer l’utilisateur à réallouer la zone mémoire.

La zone mémoire peut contenir des structures de données complexes qui se composent de plusieurs pointeurs. Étant donné que la zone mémoire est contiguë, l’application n’a pas besoin d’effectuer plusieurs appels pour libérer individuellement chaque pointeur et structure. Au lieu de cela, il peut allouer ou libérer la zone mémoire avec un appel à l’allocation de mémoire ou à la routine libre.

La mémoire tampon doit être un paramètre en [**\[ sortie \]**](out-idl.md)seule, tandis que la longueur de la mémoire tampon en octets doit être un paramètre [**\[ en \]**](in.md)uniquement.

Spécifiez une mémoire tampon suffisamment grande pour contenir tous les paramètres de [**\[ sortie \]**](out-idl.md) . En raison du remplissage masqué, utilisez des surestimations plutôt que des nombres exacts. Par exemple, les pointeurs de 4 octets sont démarshalés sur une limite alignée sur 4 octets sur les plateformes 32 bits et les pointeurs de 8 octets sur une limite de 8 octets sur les plateformes 64 bits. Par conséquent, le remplissage de l’alignement effectué par les stubs doit être comptabilisé dans l’espace de la mémoire tampon. En outre, les niveaux de compression utilisés pendant la compilation en langage C peuvent varier. Utilisez une valeur de nombre d’octets qui tient compte des octets de compression supplémentaires ajoutés au niveau de compactage utilisé lors de la compilation en langage C. Une pratique sûre qui couvre à la fois les plateformes 32 bits et les plateformes 64 bits consiste à supposer que chaque objet entrant dans le bloc Big Memory commence à une adresse qui est un multiple de 8.

## <a name="examples"></a>Exemples

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[**la longueur \_ est**](length-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**la taille \_ est**](size-is.md)
</dt> </dl>

 

 




