---
title: Attribut represent_as
description: L’attribut \ represent \_ As \ vous permet de spécifier la manière dont un type de données transmissible particulier est représenté à l’application.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- Appel de procédure distante RPC, attributs, represent_as
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311418"
---
# <a name="the-represent_as-attribute"></a>L' \_ attribut représente en tant que

L' \[ attribut [dereprésente \_ comme](/windows/desktop/Midl/represent-as) \] attribut vous permet de spécifier la manière dont un type de données transmissible particulier est représenté à l’application. Pour ce faire, spécifiez le nom du type représenté pour un type transmissible connu et fournissez les routines de conversion. Vous devez également fournir les routines pour libérer la mémoire utilisée par les objets de type de données.

Utilisez l’attribut « **\[ représenter \_ en tant que \]** » pour présenter une application avec un type de données différent, éventuellement non transmissible, plutôt que le type réellement transmis entre le client et le serveur. Il est également possible que le type manipulé par l’application ne soit pas connu au moment de la compilation MIDL. Lorsque vous choisissez un type transmissible bien défini, vous ne devez pas vous préoccuper de la représentation des données dans l’environnement hétérogène. L’attribut « **\[ représenter \_ en tant que \]** » peut améliorer l’efficacité de votre application en réduisant la quantité de données transmises sur le réseau.

L’attribut **\[ dereprésente \_ \] comme** attribut est semblable à l' \[ attribut [transmit \_ As](/windows/desktop/Midl/transmit-as) \] . Toutefois, lors de la **\[ transmission \_ en tant que \]** vous permet de spécifier un type de données qui sera utilisé pour la **\[ \_ \] transmission, representer** en tant que vous permet de spécifier la façon dont un type de données est représenté pour l’application. Le type représenté n’a pas besoin d’être défini dans les fichiers traités MIDL ; Il peut être défini au moment où les stubs sont compilés avec le compilateur C. Pour ce faire, utilisez la directive include dans le fichier de configuration de l' [application (ACF)](the-application-configuration-file-acf-.md) pour compiler le fichier d’en-tête approprié. Par exemple, le ACF suivant définit un type local pour l’application, **\_ type repr**, pour le type transmissible **nommé \_ type :**

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

Le tableau suivant décrit les quatre routines fournies par le programmeur.



| Routine                      | Description                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| **\_type nommé \_ à partir de l' \_ local** | Alloue une instance du type de réseau et convertit le type local en type de réseau.      |
| **\_type nommé \_ en \_ local**   | Convertit du type de réseau en type local.                                                    |
| **\_type nommé \_ \_ local libre** | Libère la mémoire allouée par un appel **au \_ type nommé \_ dans \_** la routine locale, mais pas le type lui-même. |
| **\_type nommé \_ Free \_ inst**  | Libère le stockage pour le type de réseau (les deux côtés).                                                     |



 

En dehors de ces quatre routines fournies par le programmeur, le type nommé n’est pas manipulé par l’application. Le seul type visible pour l’application est le type représenté. L’application utilise le nom de type représenté au lieu du nom de type transmis dans les prototypes et les stubs générés par le compilateur. Vous devez fournir le jeu de routines pour les deux côtés.

Pour les objets de **\_ type nommé** temporaires, le stub appelle le **\_ type nommé \_ Free \_ inst** pour libérer toute mémoire allouée par un appel à un **\_ type nommé \_ à partir de \_** l’état local.

Si le type représenté est un pointeur ou contient un pointeur, le **\_ type nommé \_ à \_** la routine locale doit allouer de la mémoire pour les données auxquelles les pointeurs pointent (l’objet de type représenté lui-même est manipulé de la manière habituelle). Pour \[ [les](/windows/desktop/Midl/out-idl) \] paramètres out et \[ [in](/windows/desktop/Midl/in), out \] d’un type qui contiennent une **\[ représentation \_ sous la forme** ou l’un de ses composants, la routine **\_ \_ \_ locale libre de type nommé** est automatiquement appelée pour les objets de données qui contiennent l’attribut. Pour les paramètres **\[ in \]** , la routine **\_ \_ \_ locale Free de type nommé** est appelée uniquement si l’attribut **\[ dereprésente \_ comme \]** attribut a été appliqué au paramètre. Si l’attribut a été appliqué aux composants du paramètre, la routine *\* *** \_ Free \_ local** n’est pas appelée. Les routines de libération ne sont pas appelées pour les données incorporées et les appels au plus une fois (associés à l’attribut de niveau supérieur) pour un paramètre **\[ in \]** only.

> [!Note]  
> Il est possible d’appliquer à la fois les attributs **\[ transmit \_ As \]** et **\[ \_ \] DEFAUT au même** type. Lors du marshaling des données, la **\[ représentation \_ en tant que \]** conversion de type est appliquée en premier, puis la **\[ transmission \_ comme \]** conversion est appliquée. L’ordre est inversé lors de l’annulation du marshaling des données. Ainsi, lors du marshaling, \* *_\_ à partir de \_ local_* alloue une instance d’un type nommé et la convertit d’un objet de type local en objet de type nommé temporaire. Cet objet est l’objet de type présenté utilisé pour la \* procédure *_\_ de transmission de \__* la routine. Le \* *_\_ à \__* la place de la routine alloue ensuite un objet de type transmis et le convertit de l’objet (nommé) présenté à l’objet transmis.

 

Un tableau d’entiers longs peut être utilisé pour représenter une liste liée. De cette façon, l’application manipule la liste et la transmission utilise un tableau d’entiers longs lorsqu’une liste de ce type est transmise. Vous pouvez commencer par un tableau, mais l’utilisation d’une construction avec un tableau ouvert d’entiers longs est plus pratique. L’exemple suivant vous montre comment procéder.

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

Notez que les prototypes des routines qui utilisent le type **LONGARR** sont réellement affichés dans les fichiers stub. h en tant **que \_ boîte de PLOC** à la place du type **LONGARR** . Il en va de même pour les stubs appropriés dans le \_ fichier c. c du stub.

Vous devez fournir les quatre fonctions suivantes :

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

Les routines indiquées ci-dessus effectuent les opérations suivantes :

-   Le **LONGARR \_ de \_** la routine locale compte les nœuds de la liste, alloue un objet LONGARR avec la taille **sizeof**(**LONGARR**) + Count \* *_sizeof_*(**long**), définit le champ **Size** sur Count et copie les données dans le champ **DataArr** .
-   La routine **LONGARR \_ à \_ local** crée une liste avec des nœuds de taille et transfère le tableau aux nœuds appropriés.
-   La routine **LONGARR \_ Free \_ inst** ne libère rien dans ce cas.
-   La **routine \_ \_ locale libre LONGARR** libère tous les nœuds de la liste.

 

 