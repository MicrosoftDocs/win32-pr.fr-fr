---
title: Règles de marshaling pour user_marshal et wire_marshal
description: La spécification OSF-DCE pour le marshaling des types de pointeurs incorporés exige que vous observiez les restrictions suivantes lors de l’implémentation des fonctions type d' \_ utilisateur, type \_ UserMarshal et type \_ UserUnMarshal.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97f073a5745570aae5c52d4a61d2454b960d77a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883822"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a>Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble

La spécification OSF-DCE pour le marshaling des types de pointeurs incorporés exige que vous observiez les restrictions suivantes lors de l’implémentation des &lt; fonctions type d' &gt; \_ utilisateur, &lt; type &gt; \_ UserMarshal et &lt; type &gt; \_ UserUnMarshal. (Les règles et les exemples fournis ici sont pour le marshaling. Toutefois, vos routines de dimensionnement et de démarshaling doivent respecter les mêmes restrictions) :

-   Si le type de câble est un type plat sans pointeurs, votre routine de marshaling pour le type utilisateur correspondant doit simplement marshaler les données en fonction de la disposition du type de câble. Par exemple :

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    Notez que le type de câble **long** est un type plat. Le handle de la \_ \_ fonction UserMarshal marshale une **valeur de type long** chaque fois qu’un \_ objet descripteur de handle lui est passé.

-   Si le type de câble est un pointeur vers un autre type, votre routine de marshaling pour le type utilisateur correspondant doit marshaler les données en fonction de la disposition du type vers lequel pointe le type de réseau. Le moteur de NDR s’occupe du pointeur. Par exemple :

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    Notez que le type de câble **, \_ type de câble**, est un type pointeur. Votre fonction de gestion de \_ données \_ UserMarshal marshale les données associées au handle, à l’aide de la disposition HDATA, plutôt que de la \* disposition HDATA.

-   Un type de câble doit être un type de données plat ou un type pointeur. Si votre type transmissible doit être autre chose (une structure avec des pointeurs, par exemple), utilisez un pointeur vers le type souhaité comme type de câble.

L’effet de ces restrictions est que les types définis avec les attributs de marshaling de \[ [**câble \_**](/windows/desktop/Midl/wire-marshal) \] ou d' \[ [**utilisateur \_**](/windows/desktop/Midl/user-marshal) \] peuvent être incorporés librement dans d’autres types.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Marshal de câble \_**](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**Marshal d’utilisateur \_**](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[La fonction type d' \_ utilisateur](the-type-usersize-function.md)
</dt> <dt>

[Type \_ UserMarshal (fonction)](the-type-usermarshal-function.md)
</dt> <dt>

[Thetype \_ UserUnMarshalFunction](the-type-userunmarshal-function.md)
</dt> <dt>

[Thetype \_ UserFreeFunction](the-type-userfree-function.md)
</dt> </dl>

 

 
