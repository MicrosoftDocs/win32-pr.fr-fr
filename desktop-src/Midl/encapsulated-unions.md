---
title: Unions encapsulées
description: Une Union qui est contenue avec son discriminante dans une structure dans est une Union encapsulée.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- types de données MIDL, unions encapsulées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc8f8f830d49430551af7d6450b0174742b9436afcdba764e9fa6494c957d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895359"
---
# <a name="encapsulated-unions"></a>Unions encapsulées

Une Union qui est contenue avec son discriminante dans une structure dans est une Union encapsulée. L’Union encapsulée est indiquée par la présence du mot clé [**switch**](switch.md) . Ce type d’Union est donc nommé, car le compilateur MIDL encapsule automatiquement l’Union et son discriminante dans une structure de transmission pendant un appel de procédure distante.

Si la balise Union est manquante ( \_ type U1 dans l’exemple ci-dessus), le compilateur génère la structure avec le champ d’Union nommé *\_ Union avec balises*.

La forme des unions doit être la même sur toutes les plateformes pour garantir l’interconnexion.

Pour obtenir une description de la forme d’une Union encapsulée, consultez [**Union**](union.md).

## <a name="examples"></a>Exemples

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

Pour obtenir des informations connexes, consultez [types de base MIDL](midl-base-types.md), [**char**](char-idl.md), **\[** [**\_ descripteur de contexte**](context-handle.md) **\]** , [**enum**](enum.md), **\[** [**First \_ is**](first-is.md) **\]** , **\[** [**handle**](handle.md) **\]** , **\[** [**ignore**](ignore.md) **\]** [**int**](int.md), **\[** [**ignore**](ignore.md), **\]** **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md), **\]** **\[** [**MS \_ Union**](ms-union-attrib.md) **\]** , [unencapsulated unions](nonencapsulated-unions.md), **\[** [**ptr**](ptr.md) **\]** , **\[** [**ref**](ref.md) **\]** , **\[** [**size \_ is**](size-is.md), **\]** **\[** [**String**](string.md) **\]** , [**struct**](struct.md), [**switch**](switch.md), **\[** [**Switch \_ is**](switch-is.md) **\]** , **\[** [**Switch \_ type**](switch-type.md) **\]** , **\[** [**transmit \_ As**](transmit-as.md) **\]** , [**Union**](union.md)et **\[** [**unique**](unique.md)**\]**

 

 




