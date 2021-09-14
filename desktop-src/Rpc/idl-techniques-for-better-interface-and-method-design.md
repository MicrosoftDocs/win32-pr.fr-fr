---
title: Techniques IDL pour une meilleure conception d’interface et de méthode
description: Envisagez d’utiliser les techniques spécifiques IDL suivantes pour améliorer la sécurité et les performances lorsque vous développez des interfaces et des méthodes RPC qui gèrent des données conformes et variants.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b897d8d1f2f5e1c11a5328fb095341871e3689e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194211"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a>Techniques IDL pour une meilleure conception d’interface et de méthode

Envisagez d’utiliser les techniques spécifiques IDL suivantes pour améliorer la sécurité et les performances lorsque vous développez des interfaces et des méthodes RPC qui gèrent des données conformes et variants. Les attributs référencés dans cette rubrique sont les attributs IDL définis sur les paramètres de méthode qui gèrent les données conformes (par exemple, les \[ attributs **size \_ is** \] et \[ **Max \_ is** \] ) ou des données variant (par exemple, la \[ **longueur \_ est** \] et les attributs de \[ **chaîne** \] ).

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a>Utilisation de \[ l' \] attribut Range avec des paramètres de données conformes

L' \[  \] attribut Range indique au runtime RPC d’effectuer une validation de taille supplémentaire pendant le processus d’démarshaling de données. En particulier, il vérifie que la taille fournie des données passées en tant que paramètre associé est comprise dans la plage spécifiée.

L' \[ attribut de **plage** \] n’affecte pas le format de câble.

Si la valeur du câble est en dehors de la plage autorisée, RPC lève une \_ exception RPC x \_ non valide \_ ou une exception de données de \_ \_ stub incorrecte \_ \_ RPC x. Cela fournit un niveau supplémentaire de validation des données et peut aider à éviter des erreurs de sécurité courantes telles que les dépassements de mémoire tampon. De même, l’utilisation \[  \] de Range peut améliorer les performances de l’application, car les données conformes marquées avec elle ont des contraintes clairement définies à prendre en compte par le service RPC.

## <a name="rpc-server-stub-memory-management-rules"></a>Règles de gestion de la mémoire stub du serveur RPC

Il est important de comprendre les règles de gestion de mémoire stub du serveur RPC lors de la création des fichiers IDL pour une application prenant en charge RPC. Les applications peuvent améliorer l’utilisation des ressources du serveur à l’aide \[  \] de Range conjointement avec les données conformes comme indiqué ci-dessus, et éviter délibérément l’application d’attributs d’IDL de données de longueur variable tels que la longueur comme les \[ **\_** \] données conformes.

L’application de la \[ **longueur \_** \] à des champs de structure de données définis dans un fichier IDL n’est pas recommandée.

## <a name="best-practices-for-variable-length-data-parameters"></a>Meilleures pratiques pour les paramètres de données de longueur variable

Voici quelques-unes des meilleures pratiques à prendre en compte lors de la définition des attributs IDL pour les structures de données de taille variable, les paramètres de méthode et les champs.

-   Utilisez la corrélation précoce. Il est généralement préférable de définir le champ ou le paramètre de taille de variable de façon à ce qu’il se produise immédiatement après le type intégral de contrôle.

    Par exemple,

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    est mieux que

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    où **earlyCorr** déclare le paramètre size juste avant le paramètre de données de longueur variable, et **lateCorr** déclare le paramètre size après. L’utilisation de la correspondance précoce améliore globalement les performances, en particulier dans les cas où la méthode est fréquemment appelée.

-   Pour les paramètres marqués avec l’option \[ **out, la taille \_ est** un \] tuple d’attribut et où la longueur des données est connue côté client ou où le client a une limite supérieure raisonnable, la définition de la méthode doit être similaire à ce qui suit, en termes d’attribution de paramètre et de séquence :

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    Dans ce cas, le client fournit une mémoire tampon de taille fixe pour *pArr*, ce qui permet au service RPC côté serveur d’allouer une mémoire tampon de taille raisonnable avec un bon niveau d’assurance. Notez que dans l’exemple, les données sont reçues à partir du serveur ( \[ **out** \] ). La définition est similaire pour les données passées au serveur ( \[ **dans** \] ).

-   Dans les situations où le composant côté serveur d’une application RPC détermine la longueur des données, la définition de la méthode doit ressembler à ce qui suit :

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    **Plage \_ LONG** est un type défini pour les stubs client et serveur, et d’une taille spécifiée que le client peut anticiper correctement. Dans l’exemple, le client passe *ppArr* comme **null**, et le composant d’application serveur RPC alloue la quantité de mémoire correcte. Lors du retour, le service RPC côté client alloue la mémoire pour les données retournées.

-   Si le client souhaite envoyer un sous-ensemble d’un grand tableau conforme au serveur, l’application peut spécifier la taille du sous-ensemble, comme illustré dans l’exemple suivant :

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    De cette façon, RPC transmet uniquement les éléments *lLength* du tableau sur le réseau. Toutefois, cette définition force le service RPC à allouer de la mémoire de taille *lSize* côté serveur.

-   Si le composant d’application cliente détermine la taille maximale d’un tableau que le serveur peut retourner, mais permet au serveur de transmettre un sous-ensemble de ce tableau, l’application peut spécifier un tel comportement en définissant l’IDL similaire à l’exemple suivant :

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    Le composant d’application cliente spécifie la taille maximale du tableau, et le serveur spécifie le nombre d’éléments qu’il transmet au client.

-   Si le composant d’application serveur doit retourner une chaîne au composant d’application cliente, et si le client sait que la taille maximale doit être retournée à partir du serveur, l’application peut utiliser un type de chaîne conforme, comme illustré dans l’exemple suivant :

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   Si le composant de l’application cliente ne doit pas contrôler la taille de la chaîne, le service RPC peut allouer spécifiquement la mémoire, comme illustré dans l’exemple suivant :

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    Le composant d’application cliente doit affecter à *ppStr* la **valeur null** lors de l’appel de la méthode RPC.

 

 




