---
title: attribut de rappel
description: L’attribut \ callback \ déclare une fonction de rappel statique qui existe du côté client de l’application distribuée. Les fonctions de rappel permettent au serveur d’exécuter du code sur le client.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- MIDL, attribut de rappel
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381892"
---
# <a name="callback-attribute"></a>attribut de rappel

L’attribut **\[ callback \]** déclare une fonction de rappel statique qui existe du côté client de l’application distribuée. Les fonctions de rappel permettent au serveur d’exécuter du code sur le client.

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*function-attr-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont **\[** [**local**](local.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**chaîne**](string.md) **\]** , **\[** [**Ignorer**](ignore.md) **\]** et **\[** [**\_ handle de contexte**](context-handle.md) **\]** . Séparez plusieurs attributs par des virgules.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie [un \_ type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*ptr-déclarateur* 
</dt> <dd>

Spécifie zéro ou plusieurs déclarateurs de pointeur. Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs directionnels, attributs de champ, attributs d’utilisation et attributs de pointeur appropriés pour le type de paramètre spécifié. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*declarator* 
</dt> <dd>

Spécifie un déclarateur C standard, comme des identificateurs, des déclarateurs de pointeurs et des déclarateurs de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers). L’identificateur de nom de paramètre est facultatif.

</dd> </dl>

## <a name="remarks"></a>Notes

La fonction de **\[ rappel \]** est utile lorsque le serveur doit obtenir des informations à partir du client. Si les applications serveur étaient prises en charge sur Windows 3. *x*, le serveur peut passer un appel à une procédure distante sur Windows 3. *x* Server pour obtenir les informations nécessaires. La fonction de rappel remplit la même fonction et permet au serveur d’interroger le client à la recherche d’informations dans le contexte de l’appel d’origine.

Les rappels sont des cas spéciaux d’appels distants qui s’exécutent dans le cadre d’un thread unique. Un rappel est émis dans le contexte d’un appel distant. Toute procédure distante définie dans le cadre de la même interface que la fonction de rappel statique peut appeler la fonction de rappel.

Il est important de noter qu’il n' \[ est pas recommandé d’utiliser le rappel \] dans la programmation multithread. En tant que fonction de programmation à thread unique, elle n’est pas conçue pour prendre en charge les demandes de sécurité fournies par un environnement multithread.

La fonction **RpcCancelThread** ne peut pas être utilisée pour annuler un appel qui peut distribuer un rappel statique. Si un appel de procédure distante particulier n’entraîne jamais de rappel, il peut être annulé. Dans le cas contraire, un appel peut être annulé uniquement s’il peut être garanti qu’un rappel n’a pas été émis.

Seules les séquences orientées connexion et de protocole local prennent en charge l’attribut de rappel. La taille des \[ données sortantes \] pour les rappels sur la séquence de protocole local est limitée à 150 octets. Si une interface RPC utilise une séquence de protocole sans connexion (datagramme), les appels aux procédures avec l’attribut de rappel échouent.

Les handles ne peuvent pas être utilisés en tant que paramètres dans les fonctions de rappel. Étant donné que les rappels s’exécutent toujours dans le contexte d’un appel, le handle de liaison utilisé par le client pour effectuer l’appel au serveur est également utilisé comme handle de liaison du serveur au client.

Les rappels peuvent être imbriqués à n’importe quelle profondeur.

## <a name="examples"></a>Exemples

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[**variables**](enum.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**tenir**](ignore.md)
</dt> <dt>

[**localisé**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> <dt>

[**modélis**](struct.md)
</dt> <dt>

[**UE**](union.md)
</dt> <dt>

[**unique**](unique.md)
</dt> <dt>

[**RpcCancelThread**](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 