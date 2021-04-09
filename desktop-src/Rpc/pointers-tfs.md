---
title: Pointeurs (RPC)
description: Pointeurs
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cabf5109506bc1e194a39c809bfb43a8f952fbf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102652"
---
# <a name="pointers-rpc"></a>Pointeurs (RPC)

## <a name="common-pointers"></a>Pointeurs communs

Un pointeur commun est défini comme tout autre que les pointeurs d’interface et les pointeurs de nombre d’octets.

Il existe deux dispositions possibles pour la description :

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

–ou–

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

Le premier format est utilisé si le pointeur est un pointeur vers un type simple ou un pointeur de chaîne non dimensionné. Le deuxième format est utilisé pour les pointeurs vers tous les autres types. Les attributs de pointeur indiquent la disposition de description avec l' \_ indicateur de pointeur simple FC \_ .

\_le type de pointeur<1> est l’un des éléments suivants.



| Caractère de format | Description                              |
|------------------|------------------------------------------|
| Fibre Channel \_ RP           | Pointeur de référence.                     |
| haut de la fibre \_           | Pointeur unique.                        |
| \_FP FC           | Pointeur complet.                          |
| \_op FC           | Pointeur unique dans une interface d’objet. |



 

La raison de la distinction entre FC \_ op est sémantique : dans les interfaces d’objet, un \[ pointeur in, out \] doit être libéré avant d’annuler le marshaling d’un nouvel objet et d’assigner une nouvelle valeur de pointeur.

Les \_ attributs de pointeur<1> peuvent avoir l’un des indicateurs répertoriés dans le tableau suivant.



| Indicateur | Description              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01   | FC- \_ allouer \_ tous les \_ nœuds | Le pointeur fait partie d’un schéma d’allocation Allocate (tous les \_ nœuds).                                                                                                                                                                   |
| 02   | FC n’est pas \_ \_ libre           | Pointeur Allocate (ne pas \_ libérer).                                                                                                                                                                                                      |
| 04   | FC \_ alloué \_ sur la \_ pile   | Pointeur dont le référent est alloué sur la pile du stub.                                                                                                                                                                            |
| 08   | \_pointeur simple \_ FC      | Pointeur vers un type simple ou une chaîne conforme non dimensionnée. Cet indicateur défini indique la disposition de la description du pointeur comme disposition simple du pointeur décrite ci-dessus, sinon le format du descripteur avec l’offset est indiqué. |
| 10   | \_Deref du pointeur FC \_       | Pointeur qui doit être déréférencé avant de gérer le référent du pointeur.                                                                                                                                                           |



 

Les pointeurs dont la taille \_ est (), Max \_ is (), Length \_ est (), Last \_ is () et/ou First \_ est () s’y appliquent des descriptions de chaîne de format identiques à un pointeur vers un tableau du type approprié (par exemple, un tableau conforme si la taille est \_ () est appliquée, un tableau variable conforme si la taille \_ est () et si la longueur est \_ appliquée).

## <a name="interface-pointers"></a>Pointeurs d’interface

Une chaîne de format de pointeur d’interface d’objet a l’un des deux formats, selon que l’IID correspondant est connu du compilateur ou non.

Un pointeur d’interface avec un IID de constante a la description suivante :

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

L’IID<16> composant est l’IID réel du pointeur d’interface. L’IID est écrit dans la chaîne de format dans un format identique à la structure de données GUID : long, Short, Short, char \[ 8 \] .

La description d’un pointeur d’interface avec IID \_ est () appliquée à celle-ci :

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

La \_ Description iid<> est un descripteur de corrélation et contient 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non. La valeur calculée par la fonction **NdrComputeConformance** est le pointeur iid.

## <a name="byte-count-pointers"></a>Pointeurs de nombre d’octets

Les pointeurs de nombre d’octets sont liés à un attribut d’optimisation spécial appelé \[ **\_ nombre d’octets** \] . Les formats suivants sont utilisés :

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

les

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

La \_ Description du nombre \_ d’octets<> est un descripteur de corrélation et contient 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non.

La description du pointee \_<> est une description du type de point.

 

 
