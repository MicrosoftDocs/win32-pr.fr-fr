---
title: Attribut transmit_as
description: L’attribut \ transmit \_ As \ offre un moyen de contrôler le marshaling des données sans se soucier du marshaling des données à un niveau bas \ 8212 ; autrement dit, sans vous soucier de la taille des données ou de l’échange d’octets dans un environnement hétérogène.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- Appel de procédure distante RPC, attributs, transmit_as
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096489"
---
# <a name="the-transmit_as-attribute"></a>L' \_ attribut transmit As

L' **\[** attribut [**transmettre \_ en tant que**](/windows/desktop/Midl/transmit-as) **\]** offre un moyen de contrôler le marshaling des données sans se soucier du marshaling des données à un niveau faible, autrement dit, sans se soucier de la taille des données ou de l’échange d’octets dans un environnement hétérogène. En vous permettant de réduire la quantité de données transmises sur le réseau, l’attribut **\[ transmit \_ As \]** peut rendre votre application plus efficace.

L’attribut **\[ transmettre \_ en tant \] que** permet de spécifier un type de données que les stubs RPC transmettront sur le réseau au lieu d’utiliser le type de données fourni par l’application. Vous fournissez des routines qui convertissent le type de données vers et à partir du type utilisé pour la transmission. Vous devez également fournir des routines pour libérer la mémoire utilisée pour le type de données et le type transmis. Par exemple, le code suivant définit le **\_ type** de transmission en tant que type de données transmis pour toutes les données d’application spécifiées comme étant de type **\_ spec**:

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

Le tableau suivant décrit les quatre noms de routine fournis par le programmeur. **Type** est le type de données connu de l’application, **et le type de \_ transmission est** le type de données utilisé pour la transmission.



| Routine                                                 | Description                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**type \_ à transtransmission \_**](the-type-to-xmit-function.md)     | Alloue un objet du type transmis et convertit le type d’application en type transmis sur le réseau (appelant et objet appelé). |
| [**Type \_ à partir de l' \_ émetteur**](the-type-from-xmit-function.md) | Convertit le type transmis en type d’application (appelant et objet appelé).                                                                  |
| [**Tapez \_ Free \_ inst**](the-type-free-inst-function.md) | Libère les ressources utilisées par le type d’application (objet appelé uniquement).                                                                              |
| [**Type de transmission \_ libre \_**](the-type-free-xmit-function.md) | Libère le stockage retourné par le **type** _\__ *_à \__* la routine de transmission (appelant et objet appelé).                                                      |



 

En dehors de ces quatre fonctions fournies par le programmeur, le type transmis n’est pas manipulé par l’application. Le type transmis est défini uniquement pour déplacer des données sur le réseau. Une fois les données converties dans le type utilisé par l’application, la mémoire utilisée par le type transmis est libérée.

Ces routines fournies par le programmeur sont fournies par le client ou l’application serveur en fonction des attributs directionnels. Si le paramètre est **\[** uniquement [**dans**](/windows/desktop/Midl/in) **\]** , le client transmet au serveur. Le client a besoin du type pour fournir des fonctions **\_ de \_** transmission **\_ gratuites \_** et de type. Le serveur a besoin **du \_ type \_ à partir des fonctions de** transmission et de **type \_ Free \_ inst** . Pour un **\[** paramètre en [**sortie**](/windows/desktop/Midl/out-idl) **\]** seule, le serveur transmet au client. L’application serveur doit implémenter **le \_ type \_ pour** transmettre et taper des fonctions de transmission **\_ \_ gratuites** , tandis que le programme client doit fournir le **type \_ à partir de \_** la fonction de transmission. Pour les objets **de \_ type** de transmission temporaire, le stub appelle le **type** de transmission _\__ *_\_ libre_* pour libérer toute mémoire allouée par un appel de **type \_ à \_** la transmission.

Certaines instructions s’appliquent à l’instance de type d’application. Si le type d’application est un pointeur ou contient un pointeur, le **type** \_ **de \_** la routine de transmission doit allouer de la mémoire pour les données sur lesquelles les pointeurs pointent (l’objet de type d’application lui-même est manipulé de la façon habituelle).

Pour les paramètres **\[ out \]** et **\[ in \] , \] out** , ou l’un de leurs composants, d’un type qui contient l’attribut **\[ transmit \_ As \]** , **la** \_ routine **Free \_ inst** est appelée automatiquement pour les objets de données qui ont l’attribut. Pour les paramètres **in** , **la** \_ routine **Free \_ inst** est appelée uniquement si l’attribut **\[ transmit \_ As \]** a été appliqué au paramètre. Si l’attribut a été appliqué aux composants du paramètre, le **type** \_ **Free \_ inst** routine n’est pas appelé. Il n’y a aucun appel de libération pour les données incorporées et un appel au maximum (lié à l’attribut de niveau supérieur) pour un paramètre **in** only.

Efficace avec MIDL 2,0, le client et le serveur doivent fournir les quatre fonctions. Par exemple, une liste liée peut être transmise sous la forme d’un tableau de taille. Le **type \_ à \_** la routine de transmission parcourt la liste liée et copie les données ordonnées dans un tableau. Les éléments du tableau sont triés de sorte que les nombreux pointeurs associés à la structure de la liste n’ont pas besoin d’être transmis. Le **type \_ de \_** la routine de transmission lit le tableau et place ses éléments dans une structure de liste liée.

La liste \_ à double liaison (liste de liens doubles \_ ) comprend des données et des pointeurs vers les éléments de la liste précédente et suivante :

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

Au lieu d’expédier la structure complexe, l' **\[** attribut [**transmit \_ As**](/windows/desktop/Midl/transmit-as) **\]** peut être utilisé pour l’envoyer sur le réseau sous forme de tableau. La séquence d’éléments dans le tableau conserve l’ordre des éléments dans la liste à un coût inférieur :

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

L’attribut **\[ transmit \_ As \]** apparaît dans le fichier IDL :

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

Dans l’exemple suivant, **ModifyListProc** définit le paramètre de type double \_ Link \_ comme un paramètre **\[ in, out \]** :

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

Les quatre fonctions définies par le programmeur utilisent le nom du type dans les noms de fonction, et utilisent les types présentés et transmis comme types de paramètres, selon les besoins :

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 