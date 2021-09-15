---
title: Gestion de la mémoire stub serveur
description: Gestion de la mémoire stub serveur
ms.assetid: 99e3ee56-5adb-4b25-bcf2-316d1bbdbdba
keywords:
- Gestion de la mémoire stub serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e052df6da999e5371ac498a1d39852b4be2b5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413521"
---
# <a name="server-stub-memory-management"></a>Gestion de la mémoire stub serveur

## <a name="an-introduction-to-server-stub-memory-management"></a>Présentation de la gestion de la mémoire Server-Stub

Les stubs générés par MIDL jouent le rôle d’interface entre un processus client et un processus serveur. Un stub client marshale toutes les données passées aux paramètres marqués avec l’attribut [**\[ in \]**](../midl/in.md) , puis les envoie au stub serveur. Le stub de serveur, lors de la réception de ces données, reconstruit la pile des appels, puis exécute la fonction de serveur implémentée par l’utilisateur correspondante. Le stub serveur marshale également les données de paramètre marquées avec l’attribut [**\[ out \]**](../midl/out-idl.md) et les retourne à l’application cliente.

Le format de données marshalé 32 bits utilisé par MSRPC est une version conforme de la syntaxe de transfert de représentation de données réseau (NDR). Pour plus d’informations sur ce format, consultez [le site Web du groupe ouvert](https://www.opengroup.org/). Pour les plateformes 64 bits, une extension Microsoft 64 bits à la syntaxe de transfert NDR appelée NDR64 peut être utilisée pour de meilleures performances.

## <a name="unmarshaling-inbound-data"></a>Démarshaling de données entrantes

Dans MSRPC, le stub client marshale toutes les données de paramètre marquées comme [**\[ dans \]**](../midl/in.md) dans une mémoire tampon continue pour la transmission au stub serveur. De même, le stub serveur marshale toutes les données marquées avec l’attribut [**\[ out \]**](../midl/out-idl.md) dans une mémoire tampon continue pour revenir au stub client. Alors que la couche de protocole réseau sous RPC peut fragmenter et transmettre la mémoire tampon à la transmission, la fragmentation est transparente pour les stubs RPC.

L’allocation de mémoire pour la création de la trame d’appel du serveur peut être une opération coûteuse. Le stub serveur tentera de réduire l’utilisation de mémoire inutile si possible, et il est supposé que la routine de serveur ne libérera pas ou ne réalloue pas de données marquées avec les attributs [**\[ in \]**](../midl/in.md) ou **\[ in, out \]** . Chaque fois que cela est possible, le stub serveur tente de réutiliser les données dans la mémoire tampon afin d’éviter toute duplication inutile. La règle générale est que si le format de données marshalé est le même que celui de la mémoire, RPC utilise des pointeurs vers les données regroupées au lieu d’allouer de la mémoire supplémentaire pour les données mises en forme de manière identique.

Par exemple, l’appel RPC suivant est défini avec une structure dont le format marshalé est identique à son format en mémoire.

``` syntax
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```

Dans ce cas, RPC n’alloue pas de mémoire supplémentaire pour les données référencées par *plInStructure*; au lieu de cela, il passe simplement le pointeur vers les données marshalées à l’implémentation de fonction côté serveur. Le stub du serveur RPC vérifie la mémoire tampon pendant le processus d’démarshaling si le stub est compilé à l’aide de l’indicateur « -Solid » (qui est un paramètre par défaut dans la version récente nmost du compilateur MIDL). RPC garantit que les données passées à l’implémentation de la fonction côté serveur sont valides.

N’oubliez pas que la mémoire est allouée à *plOutStructure*, car aucune donnée n’est transmise au serveur pour celle-ci.

## <a name="memory-allocation-for-inbound-data"></a>Allocation de mémoire pour les données entrantes

Des cas peuvent se produire lorsque le stub de serveur alloue de la mémoire pour les données de paramètre marquées avec les attributs [**\[ in \]**](../midl/in.md) ou **\[ in, out \]** . Cela se produit lorsque le format de données marshalé diffère du format de mémoire, ou lorsque les structures qui composent les données marshalées sont suffisamment complexes et doivent être lues de manière atomique par le stub du serveur RPC. La liste ci-dessous présente plusieurs cas courants lorsque la mémoire doit être allouée pour les données reçues par le stub serveur.

-   Les données sont un tableau variable ou un tableau variable conforme. Il s’agit de tableaux (ou de pointeurs vers des tableaux) dont la [**\[ longueur \_ est ( \] )**](../midl/length-is.md) ou le [**\[ premier attribut \_ est () \]**](../midl/first-is.md) défini sur ces derniers. Dans le rapport de non-remise, seul le premier élément de ces tableaux est marshalé et transmis. Par exemple, dans l’extrait de code ci-dessous, les données passées dans le paramètre *PV* auront une mémoire allouée.

    ``` syntax
    void RpcFunction
    (
        [in] long size,
        [in, out] long *pLength,
        [in, out, size_is(size), length_is(*pLength)] long *pv
    );
    ```

-   Les données sont une chaîne dimensionnée ou une chaîne non conforme. Ces chaînes sont généralement des pointeurs vers des données de caractères marqués avec l’attribut [**\[ size \_ is () \]**](../midl/size-is.md) . Dans l’exemple ci-dessous, la chaîne transmise à la fonction côté serveur **SizedString** aura une mémoire allouée, alors que la chaîne transmise à la fonction **NormalString** sera réutilisée.

    ``` syntax
    void SizedString
    (
        [in] long size,
        [in, size_is(size), string] char *str
    );

    void NormalString
    (
        [in, string] char str
    );
    ```

-   Les données sont un type simple dont la taille de la mémoire diffère de sa taille marshalée, par exemple **enum16** et **\_ \_ int3264**.
-   Les données sont définies par une structure dont l’alignement de la mémoire est plus petit que l’alignement naturel, contient l’un des types de données ci-dessus ou a des remplissages d’octets de fin. Par exemple, la structure de données complexe suivante a forcé l’alignement sur 2 octets et a un remplissage à la fin.

    ``` syntax
#pragma pack(2)
    typedef struct ComplexPackedStructure
    {
        char c;  
        long l;   // alignment is forced at the second byte
        char c2;  // there will be a trailing one-byte pad to keep 2-byte alignment
    }
    ```

-   Les données contiennent une structure qui doit être marshalée champ par champ. Ces champs incluent des pointeurs d’interface définis dans les interfaces DCOM. pointeurs ignorés ; valeurs entières définies avec l’attribut de [**\[ plage \]**](../midl/range.md) ; éléments de tableaux définis avec les attributs de [**\[ \_ \] marshaling de câble**](../midl/wire-marshal.md), d' [**\[ utilisateur \_ Marshal \]**](../midl/user-marshal.md), de [**\[ transmission \_ en tant \]**](../midl/transmit-as.md) que et de [**\[ représentation \_ sous forme \]**](../midl/represent-as.md) de données et structures de données complexes incorporées.
-   Les données contiennent une Union, une structure contenant une Union ou un tableau d’unions. Seule la branche spécifique de l’Union est marshalée sur le câble.
-   Les données contiennent une structure avec un tableau de conformité multidimensionnelle qui possède au moins une dimension non fixe.
-   Les données contiennent un tableau de structures complexes.
-   Les données contiennent un tableau de types de données simples tels que **enum16** et **\_ \_ int3264**.
-   Les données contiennent un tableau de pointeurs REF et interface.
-   Les données ont un attribut [**\[ force \_ allocate \]**](../midl/force-allocate.md) appliqué à un pointeur.
-   Les données ont un attribut [**\[ allocate (tous les \_ nœuds) \]**](../midl/allocate.md) appliqué à un pointeur.
-   Les données ont un attribut de [**\[ \_ nombre \] d’octets**](../midl/byte-count.md) appliqué à un pointeur.

## <a name="64-bit-data-and-ndr64-transfer-syntax"></a>64 bits et syntaxe de transfert NDR64

Comme mentionné précédemment, les données 64 bits sont marshalées à l’aide d’une syntaxe de transfert 64 bits spécifique appelée NDR64. Cette syntaxe de transfert a été développée pour résoudre le problème spécifique qui survient lorsque les pointeurs sont marshalés sous un rapport de non-résolution 32 bits et transmis à un stub serveur sur une plateforme 64 bits. Dans ce cas, un pointeur de données 32 bits marshalé ne correspond pas à une unité de 64 bits, et l’allocation de mémoire se produira invariablement. Pour créer un comportement plus cohérent sur les plateformes 64 bits, Microsoft a développé une nouvelle syntaxe de transfert appelée NDR64.

Voici un exemple illustrant ce problème :


```C++
typedef struct PtrStruct
{
  long l;
  long *pl;
}
```



Cette structure, quand elle est marshalée, est réutilisée par le stub serveur sur un système 32 bits. Toutefois, si le stub serveur réside sur un système 64 bits, les données marshalées par NDR ont une longueur de 4 octets, mais la taille de mémoire requise sera de 8. Par conséquent, l’allocation de mémoire est forcée et la réutilisation de la mémoire tampon se produit rarement. NDR64 résout ce problème en transformant la taille marshalée d’un pointeur 64 bits.

Contrairement au NDR 32 bits, les Tyes de données simples, comme **enum16** et **\_ \_ int3264** , ne rendent pas une structure ou un tableau complexe sous NDR64. De même, les valeurs de remplissage de fin ne rendent pas une structure complexe. Les pointeurs d’interface sont traités comme des pointeurs uniques au niveau supérieur ; par conséquent, les structures et les tableaux contenant des pointeurs d’interface ne sont pas considérés comme complexes et ne nécessitent pas d’allocation de mémoire spécifique pour leur utilisation.

## <a name="initializing-outbound-data"></a>Initialisation des données sortantes

Une fois que toutes les données entrantes n’ont pas été marshalées, le stub serveur doit initialiser les pointeurs sortants uniquement marqués avec l’attribut [**\[ out \]**](../midl/out-idl.md) .


```C++
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```



Dans l’appel ci-dessus, le stub serveur doit initialiser *plOutStructure* , car il n’était pas présent dans les données marshalées, et il s’agit d’un pointeur [**\[ Ref \]**](../midl/ref.md) implicite qui doit être mis à la disposition de l’implémentation de la fonction serveur. Le stub de serveur RPC initialise et zéro les pointeurs de référence uniquement de niveau supérieur avec l’attribut [**\[ out \]**](../midl/out-idl.md) . Les pointeurs de référence **\[ out \]** situés sous celui-ci sont également initialisés de manière récursive. La récursivité s’arrête à tous les pointeurs avec les attributs [**\[ uniques \]**](../midl/unique.md) ou [**\[ ptr \]**](../midl/ptr.md) définis.

L’implémentation de fonction serveur ne peut pas modifier directement les valeurs de pointeur de niveau supérieur et ne peut donc pas les réallouer. Par exemple, dans l’implémentation de **ProcessRpcStructure** ci-dessus, le code suivant n’est pas valide :


```C++
void ProcessRpcStructure(RpcStructure *plInStructure, rpcStructure *plOutStructure)
{
    plOutStructure = MIDL_user_allocate(sizeof(RpcStructure));
    Process(plOutStructure);
}
```



*plOutStructure* est une valeur de pile et sa modification n’est pas propagée vers RPC. L’implémentation de la fonction serveur peut tenter d’éviter l’allocation en tentant de libérer des *plOutStructure*, ce qui peut entraîner une altération de la mémoire. Le stub serveur allouera ensuite de l’espace pour le pointeur de niveau supérieur en mémoire (dans le cas pointeur vers pointeur) et une structure simple de niveau supérieur dont la taille sur la pile est plus petite que prévu.

Dans certains cas, le client peut spécifier la taille d’allocation de mémoire du côté serveur. Dans l’exemple suivant, le client spécifie la taille des données sortantes dans le paramètre de *taille* entrante.

``` syntax
void VariableSizeData
(
    [in] long size,
    [out, size_is(size)] char *pv
);
```

Après avoir démarshalé les données entrantes, y compris la *taille*, le stub serveur alloue une mémoire tampon pour *PV* avec une taille de « sizeof (Char) \* Size ». Une fois que l’espace a été alloué, le stub de serveur met à zéro la mémoire tampon. Notez que dans ce cas particulier, le stub alloue la mémoire avec l' **\_ allocation d’utilisateur MIDL \_ ()**, car la taille de la mémoire tampon est déterminée au moment de l’exécution.

Sachez que dans le cas des interfaces DCOM, les stubs générés par MIDL peuvent ne pas être impliqués du tout si le client et le serveur partagent le même cloisonnement COM, ou si **ICallFrame** est implémenté. Dans ce cas, le serveur ne peut pas dépendre du comportement d’allocation et doit vérifier indépendamment la mémoire dimensionnée par le client.

## <a name="server-side-function-implementations-and-outbound-data-marshaling"></a>Implémentations de fonctions côté serveur et marshaling de données sortantes

Immédiatement après le démarshaling des données entrantes et l’initialisation de la mémoire allouée pour contenir des données sortantes, le stub de serveur RPC exécute l’implémentation côté serveur de la fonction appelée par le client. À ce stade, le serveur peut modifier les données spécifiquement marquées avec l’attribut **\[ in \] , out** , et il peut remplir la mémoire allouée pour les données sortantes uniquement (les données marquées avec [**\[ out \]**](../midl/out-idl.md)).

Les règles générales de manipulation des données de paramètre marshalé sont simples : le serveur peut uniquement allouer de la mémoire ou modifier la mémoire allouée spécifiquement par le stub serveur. La réallocation ou la libération de la mémoire existante pour les données peut avoir un impact négatif sur les résultats et les performances de l’appel de fonction, et peut être très difficile à déboguer.

Logiquement, le serveur RPC réside dans un espace d’adressage différent du client, et il est généralement supposé qu’ils ne partagent pas de mémoire. Par conséquent, il est possible que l’implémentation de fonction serveur utilise les données marquées avec l’attribut [**\[ in \]**](../midl/in.md) comme mémoire « Scratch » sans affecter les adresses mémoire du client. Cela dit, le serveur ne doit pas tenter de réallouer ou **\[ de \]** libérer des données, ce qui laisse le contrôle de ces espaces au stub du serveur RPC lui-même.

En général, l’implémentation de fonction serveur n’a pas besoin de réallouer ou de libérer des données marquées avec l’attribut **\[ in, out \]** . Pour les données de taille fixe, la logique d’implémentation de la fonction peut modifier directement les données. De même, pour les données de taille variable, l’implémentation de fonction ne doit pas modifier la valeur de champ fournie à l’attribut [**\[ size \_ is () \]**](../midl/size-is.md) , soit. Modifiez la valeur de champ utilisée pour dimensionner les données dans une mémoire tampon plus petite ou plus grande retournée au client, qui peut être mal équipée pour traiter la longueur anormale.

Si des circonstances se produisent lorsque la routine du serveur doit réallouer la mémoire utilisée par les données marquées avec l’attribut **\[ in, out \]** , il est tout à fait possible que l’implémentation de la fonction côté serveur ne sache pas si le pointeur fourni par le stub est la mémoire allouée avec **MIDL \_ User \_ allocate ()** ou la mémoire tampon de câble marshalée. Pour contourner ce problème, MS RPC peut s’assurer qu’aucune fuite de mémoire ou altération n’a lieu si l’attribut [**\[ force \_ allocate \]**](../midl/force-allocate.md) est défini sur les données. Quand **\[ force \_ allocate \]** est définie, le stub serveur allouera toujours la mémoire pour le pointeur, bien que l’inconvénient est que les performances diminuent pour chaque utilisation.

Lorsque l’appel est retourné par l’implémentation de fonction côté serveur, le stub serveur marshale les données marquées avec l’attribut [**\[ out \]**](../midl/out-idl.md) et les envoie au client. N’oubliez pas que le stub ne marshale pas les données si l’implémentation de fonction côté serveur lève une exception.

## <a name="releasing-allocated-memory"></a>Libérer de la mémoire allouée

Le stub du serveur RPC libère la mémoire de la pile une fois que l’appel a été retourné par la fonction côté serveur, qu’une exception se produise ou non. Le stub serveur libère toute la mémoire allouée par le stub, ainsi que toute mémoire allouée avec l' **\_ allocation utilisateur MIDL \_ ()**. L’implémentation de fonction côté serveur doit toujours donner à RPC un état cohérent, soit en levant une exception, soit en retournant un code d’erreur. Si la fonction échoue pendant le remplissage de structures de données complexes, elle doit s’assurer que tous les pointeurs pointent vers des données valides ou ont la valeur **null**.

Pendant cette étape, le stub serveur libère toute la mémoire qui ne fait pas partie de la mémoire tampon marshalée contenant les données [**\[ dans \]**](../midl/in.md) . Il existe une exception à ce comportement : les données avec l’attribut [**\[ allocate (ne pas \_ libérer) \]**](../midl/allocate.md) défini sur elles-le stub du serveur ne libère pas de mémoire associée à ces pointeurs.

Une fois que le stub serveur libère la mémoire allouée par le stub et l’implémentation de la fonction, le stub appelle une fonction de notification spécifique si l’attribut [**\[ \_ indicateur \] Notify**](../midl/notify-flag.md) est spécifié pour des données particulières.

## <a name="marshalling-a-linked-list-over-rpc----an-example"></a>Marshaling d’une liste liée sur RPC--un exemple


```C++
typedef struct _LINKEDLIST
{
    long lSize;
    [size_is(lSize)] char *pData;
    struct _LINKEDLIST *pNext;
} LINKEDLIST, *PLINKEDLIST;

void Test
(
    [in] LINKEDLIST *pIn,
    [in, out] PLINKEDLIST *pInOut,
    [out] LINKEDLIST *pOut
);
```



Dans l’exemple ci-dessus, le format de mémoire pour **LINKEDLIST** sera identique au format de câble marshalé. Par conséquent, le stub serveur n’alloue pas de mémoire pour la chaîne entière de pointeurs de données sous le *code confidentiel*. Au lieu de cela, RPC réutilise la mémoire tampon de transmission pour l’ensemble de la liste liée. De même, le stub n’alloue pas de mémoire pour *pInOut*, mais réutilise à la place le tampon de transmission marshalé par le client.

Étant donné que la signature de fonction contient un paramètre sortant, *moue*, le stub de serveur alloue de la mémoire pour contenir les données retournées. La mémoire allouée est initialement zéro, avec **pNext** ayant la valeur **null**. L’application peut allouer la mémoire pour une nouvelle liste liée et un point *moue* -> **pNext** . *pin* et la liste liée qu’il contient peuvent être utilisées comme un espace de travail, mais l’application ne doit pas modifier les pointeurs pNext.

L’application peut modifier librement le contenu de la liste liée vers laquelle pointe *pInOut*, mais elle ne doit pas modifier les pointeurs **pNext** , sans parler du lien de niveau supérieur lui-même. Si l’application décide de raccourcir la liste liée, elle ne peut pas savoir si un pointeur **pNext** donné lie pour une mémoire tampon interne RPC ou une mémoire tampon allouée spécifiquement avec l' **allocation d' \_ utilisateur MIDL \_ ()**. Pour contourner ce problème, vous ajoutez une déclaration de type spécifique pour les pointeurs de liste liés qui forcent l’allocation des utilisateurs, comme indiqué dans le code ci-dessous.

``` syntax
typedef [force_allocate] PLINKEDLIST;
```

Cet attribut force le stub de serveur à allouer séparément chaque nœud de la liste liée, et l’application peut libérer la partie abrégée de la liste liée en appelant l' **\_ utilisateur \_ gratuit MIDL ()**. L’application peut ensuite définir en toute sécurité le pointeur **pNext** à la fin de la liste liée récemment raccourcie sur **null**.

 

 