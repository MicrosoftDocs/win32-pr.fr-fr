---
title: attribut represent_as
description: L’attribut \ \_ Renamed as \ ACF associe un type local nommé dans le repr de langage cible à un type de transfert nommé-type qui est transféré entre le client et le serveur.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as MIDL de l’attribut
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093218"
---
# <a name="represent_as-attribute"></a>représenter \_ en tant qu’attribut

L’attribut **\[ dereprésente \_ As \]** ACF associe un type local nommé dans le *repr* de langage cible à un type de transfert *nommé-type* qui est transféré entre le client et le serveur.

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type nommé* 
</dt> <dd>

Spécifie le type de données de transfert nommé qui est transféré entre le client et le serveur.

</dd> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie un ou plusieurs attributs qui s’appliquent au type. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*repr-type* 
</dt> <dd>

Spécifie le type local représenté dans la langue cible présentée aux applications clientes et serveur.

</dd> </dl>

## <a name="remarks"></a>Notes

Lors de l’utilisation de l’objet **\[ représenter \_ en tant que \]**, vous devez fournir des routines qui effectuent une conversion entre les types local et de transfert et qui libèrent de la mémoire utilisée pour stocker les données converties. L’attribut **\[ dereprésente \_ en tant que \]** indique aux stubs d’appeler les routines de conversion fournies par l’utilisateur.

Le type transféré *nommé-type* doit correspondre à un type de base MIDL, à un type prédéfini ou à un identificateur de type. Pour plus d’informations, consultez [types de base MIDL](midl-base-types.md).

Vous devez fournir les routines suivantes :



| Nom de la routine                   | Description                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *\_type nommé * * * \_ à partir de l' \_ local** | Convertit les données du type local en type de réseau. La routine alloue de la mémoire pour le type de données réseau, y compris la mémoire pour toutes les données référencées par des pointeurs dans le type de données réseau.              |
| *\_type nommé * * * \_ vers \_ local**   | Convertit les données du type de réseau en type local. La routine est chargée d’allouer de la mémoire pour les données référencées par des pointeurs dans le type local. RPC alloue de la mémoire pour le type local lui-même. |
| *\_type nommé * * * \_ libre \_ local** | Libère la mémoire allouée pour les données référencées par des pointeurs dans le type local. RPC libère de la mémoire pour le type lui-même                                                                                             |
| *\_type nommé * * * \_ gratuit \_ inst**  | Libère de la mémoire allouée pour les données référencées par des pointeurs dans le type de réseau et pour le type de réseau lui-même.                                                                                            |



 

Le stub client appelle le *type nommé * * * \_ à partir de \_ local** pour allouer de l’espace pour le type transmis et pour convertir les données du type local en type de réseau. Le stub serveur alloue de l’espace pour le type de données d’origine et appelle le type *nommé * * * \_ à \_ local** pour convertir les données du type de réseau en type local.

Lors du retour du code d’application, les stubs client et serveur appellent le *type * * * \_ Free \_ inst** pour libérer le stockage pour le type de réseau. Le stub client appelle le *type nommé * * * \_ Free \_ local** pour libérer le stockage retourné par la routine.

Les types suivants ne peuvent pas avoir un attribut **\[ dereprésente \_ comme \]** attribut :

-   Tableaux à variation variable conformes, variables ou conformes
-   Structures dans lesquelles le dernier membre est un tableau conforme (structure conforme)
-   Pointeurs ou types qui contiennent un pointeur
-   Canaux ou types qui contiennent des canaux
-   Types utilisés comme type de base pour un canal
-   Les types prédéfinis [**gèrent \_ t**](handle-t.md), [**void**](void.md)
-   Types qui ont l’attribut [**\[ handle \]**](handle.md)

## <a name="examples"></a>Exemples

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**nullité**](void.md)
</dt> </dl>

 

 




