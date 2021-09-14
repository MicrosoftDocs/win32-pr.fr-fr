---
title: attribut context_handle
description: L’attribut \ Context \_ handle \ identifie un handle de liaison qui gère le contexte, ou les informations d’État, sur le serveur entre les appels de procédure distante.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- context_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093717"
---
# <a name="context_handle-attribute"></a>attribut de handle de contexte \_

L’attribut de **\[ \_ handle \] de contexte** identifie un handle de liaison qui gère le contexte, ou les informations d’État, sur le serveur entre les appels de procédure distante.

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie un ou plusieurs attributs qui s’appliquent au type.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un type pointeur ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*déclarateur et déclarateur-liste* 
</dt> <dd>

Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. Le déclarateur d’un handle de contexte doit inclure au moins un déclarateur de pointeur. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers). La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs, séparés par des virgules. L’identificateur de nom de paramètre dans le déclarateur de fonction est facultatif.

</dd> <dt>

*function-attr-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**chaîne**](string.md) **\]** , **\[** [**Ignorer**](ignore.md) **\]** et **\[ \_ handle \] de contexte**.

</dd> <dt>

*pointeur-decl* 
</dt> <dd>

Spécifie zéro ou plusieurs déclarateurs de pointeur. Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' **\* *indicateur _, de modificateurs tels que _* Far** et du qualificateur [**const**](const.md).

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*Parameter-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs directionnels, attributs de champ, attributs d’utilisation et attributs de pointeur appropriés pour le type de paramètre spécifié. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*Context-handle-type* 
</dt> <dd>

Spécifie l’identificateur qui spécifie le type de handle de contexte tel que défini dans une déclaration [**typedef**](typedef.md) qui prend l’attribut de **\[ \_ handle \] de contexte** . La routine d’arrêt est facultative.

**Windows ServerÂ 2003 et WindowsÂ XP :** Une interface unique peut prendre en charge des handles de contexte sérialisés et non sérialisés, ce qui permet à une méthode sur une interface d’accéder exclusivement à un handle de contexte (sérialisé), tandis que d’autres méthodes accèdent à ce handle de contexte en mode partagé (non sérialisé). Ces fonctionnalités d’accès sont comparables aux mécanismes de verrouillage en lecture/écriture. les méthodes qui utilisent un handle de contexte sérialisé sont des utilisateurs exclusifs (enregistreurs), tandis que les méthodes qui utilisent un handle de contexte non sérialisé sont des utilisateurs partagés (lecteurs). Les méthodes qui détruisent ou modifient l’état d’un handle de contexte doivent être sérialisées. Les méthodes qui ne modifient pas l’état d’un handle de contexte, telles que les méthodes qui lisent simplement un handle de contexte, peuvent être non sérialisées. Notez que les méthodes de création sont implicitement sérialisées.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut de **\[ \_ handle \] de contexte** peut apparaître en tant qu’attribut de type [**typedef**](typedef.md) IDL, en tant qu’attribut de type de retour de fonction ou en tant qu’attribut de paramètre. Quand vous appliquez l’attribut de **\[ \_ handle \] de contexte** à une définition de type, vous devez également fournir une routine d’arrêt de contexte. Pour plus d’informations, consultez [routine de fonctionnement du contexte de serveur](/windows/desktop/Rpc/server-context-run-down-routine) .

Quand vous utilisez le compilateur MIDL en mode par défaut ([**/ms. \_ ext**](-ms-ext.md)), un descripteur de contexte peut être n’importe quel type pointeur sélectionné par l’utilisateur, à condition qu’il soit conforme aux exigences des handles de contexte décrits ici. Les données associées à ce type de descripteur de contexte ne sont pas transmises sur le réseau et ne doivent être manipulées que par l’application serveur. Les compilateurs IDL DCE restreignent les handles de contexte aux pointeurs de type [**void**](void.md)  * *\** _. Par conséquent, cette fonctionnalité n’est pas disponible lorsque vous utilisez le commutateur MIDL [_ */OSF* *](-osf.md) du compilateur MIDL.

Comme avec d’autres types de handles, le handle de contexte est opaque pour l’application cliente, et toutes les données qui lui sont associées ne sont pas transmises. Sur le serveur, le handle de contexte sert de handle sur le contexte actif, et toutes les données associées au type de descripteur de contexte sont accessibles.

Pour créer un handle de contexte, le client passe au serveur un **\[** [](out-idl.md) **\]** **\[** [](ref.md) **\]** pointeur Ref vers un handle de contexte. (Le handle de contexte lui-même peut avoir une valeur **null** ou non **null** , à condition que sa valeur soit cohérente avec ses attributs de pointeur. Par exemple, quand l’attribut ref est appliqué au type de handle de contexte **\[** [](ref.md) **\]** , il ne peut pas avoir de valeur **null** .) Un autre handle de liaison doit être fourni pour accomplir la liaison jusqu’à ce que le handle de contexte soit créé. Quand aucun handle explicite n’est spécifié, la liaison implicite est utilisée. Lorsqu’aucun **\[** attribut de [**\_ handle implicite**](implicit-handle.md) **\]** n’est présent, un handle automatique est utilisé.

La procédure distante sur le serveur crée un handle de contexte actif. Le client doit utiliser ce handle de contexte en tant que **\[** [](in.md) **\]** paramètre in ou **\[ in**, **out dans les \]** appels suivants. Un handle **\[ de contexte \] en** uniquement peut être utilisé comme handle de liaison, donc il doit avoir une valeur non **null** . Un handle **\[ de contexte en \]** uniquement ne reflète pas les modifications d’État sur le serveur.

Sur le serveur, la procédure appelée peut interpréter le descripteur de contexte en fonction des besoins. Par exemple, la procédure appelée peut allouer le stockage du tas et utiliser le handle de contexte comme pointeur vers ce stockage.

Pour fermer un handle de contexte, le client passe le handle de contexte en tant qu' **\[** argument [**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** . Le serveur doit retourner un handle de contexte **null** lorsqu’il ne gère plus le contexte pour le compte de l’appelant. Par exemple, si le handle de contexte représente un fichier ouvert et que l’appel ferme le fichier, le serveur doit définir le handle de contexte sur la **valeur null** et le renvoyer au client. Une valeur **null** n’est pas valide en tant que handle de liaison lors des appels suivants.

Un descripteur de contexte n’est valide que pour un seul serveur. Lorsqu’une fonction a deux paramètres de handle et que le handle de contexte n’a pas la **valeur null**, les handles de liaison doivent faire référence au même espace d’adressage.

Quand une fonction possède un **\[** handle [**de contexte in**](in.md) **\]** ou **\[ in**, **out \]** , son handle de contexte peut être utilisé comme handle de liaison. Dans ce cas, la liaison implicite n’est pas utilisée et le **\[** [**\_ handle implicite**](implicit-handle.md) **\]** ou l’attribut de **\[** [**\_ handle automatique**](auto-handle.md) **\]** est ignoré.

Les restrictions suivantes s’appliquent aux handles de contexte :

-   Les handles de contexte ne peuvent pas être des éléments de tableau, des membres de structure ou des membres d’Union. Ils peuvent uniquement être des paramètres.
-   Les handles de contexte ne peuvent pas avoir l' **\[** attribut [**transmit \_ As**](transmit-as.md) **\]** ou **\[** [**dereprésente \_ As**](represent-as.md) **\]** .
-   Les paramètres qui sont des pointeurs vers **\[** [**des**](out-idl.md) **\]** Handles de contexte doivent être des **\[** [](ref.md) **\]** pointeurs Ref.
-   Un **\[** handle [**de contexte in**](in.md) **\]** peut être utilisé comme handle de liaison et ne peut pas avoir la **valeur null**.
-   Un handle **\[ de contexte in**, [**out**](out-idl.md) peut avoir la **valeur null** en entrée, mais uniquement si la procédure a un autre paramètre de handle explicite. S’il n’existe aucun autre paramètre explicite **\[ de handle de** contexte non **null** , le handle de contexte **out \]** ne peut pas être **null**.
-   Un descripteur de contexte ne peut pas être utilisé avec les rappels.

## <a name="examples"></a>Exemples

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[**\_handle automatique**](auto-handle.md)
</dt> <dt>

[**rappel**](callback.md)
</dt> <dt>

[Réinitialisation du contexte client](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Handles de contexte](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**traitée**](handle.md)
</dt> <dt>

[Liaison et Handles](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[**ignore**](ignore.md)
</dt> <dt>

[**handle implicite \_**](implicit-handle.md)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[**localisé**](local.md)
</dt> <dt>

[Clients multithread et handles de contexte](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**/ms. \_ ext**](-ms-ext.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**représenter \_ comme**](represent-as.md)
</dt> <dt>

[**RpcSsDestroyClientContext**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[Routine d’exécution du contexte de serveur](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[**chaîne**](string.md)
</dt> <dt>

[**transmettre \_ en tant que**](transmit-as.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**unique**](unique.md)
</dt> <dt>

[**nullité**](void.md)
</dt> </dl>

 

 