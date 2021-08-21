---
title: attribut d'objet
description: L’attribut \ Object \ interface identifie une interface COM.
ms.assetid: 51e34ef3-eea7-45f4-b961-a9f742700fe5
keywords:
- MIDL (attribut d’objet)
topic_type:
- apiref
api_name:
- object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ddf51e020cdcd5d13dde6938a58ea5e51f22d9dd03f8632312b3d6b8453a9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383507"
---
# <a name="object-attribute"></a>attribut d'objet

L’attribut d’interface de l' **\[ objet \]** identifie une interface com. (Une liste d’attributs d’interface qui n’inclut pas l’attribut d' **\[ objet \]** indique une interface RPC DCE.)

``` syntax
[ 
    object, 
    uuid(string-uuid)
    [ , interface-attribute-list] 
] 
interface interface-name : base-interface
{
...    
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*chaîne-UUID* 
</dt> <dd>

Chaîne UUID générée par l’utilitaire uuidgen. Vous pouvez placer la chaîne UUID entre guillemets.

</dd> <dt>

*interface-attribut-List* 
</dt> <dd>

Autres attributs qui s’appliquent à l’ensemble de l’interface.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Nom de l’interface.

</dd> <dt>

*interface de base* 
</dt> <dd>

Interface COM dérivée de cette interface. L’interface de base doit être [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)ou une autre interface com qui dérive, directement ou indirectement, de **IUnknown** ou **IDispatch**.

</dd> </dl>

## <a name="remarks"></a>Remarques

Une liste d’attributs d’interface pour une interface COM doit inclure l' **\[** attribut [**UUID**](uuid.md) **\]** , mais elle ne peut pas inclure l' **\[** attribut [**version**](version.md) **\]** .

Par défaut, la compilation d’une interface COM avec le compilateur MIDL génère les fichiers nécessaires à la génération d’une DLL de proxy. Cette DLL contient le code permettant de prendre en charge l’utilisation de l’interface COM personnalisée à la fois par les applications clientes et les serveurs d’objets. Toutefois, si la liste d’attributs d’interface d’une interface COM spécifie l' **\[** [](local.md) **\]** attribut local, le compilateur MIDL génère uniquement le fichier d’en-tête d’interface.

Le compilateur MIDL génère automatiquement un type de données d’interface pour une interface COM. Vous pouvez également utiliser [**typedef**](typedef.md) avec le mot clé [**interface**](interface.md) pour définir explicitement un type de données d’interface. La spécification de l’interface peut ensuite utiliser le type de données de l’interface dans les paramètres de fonction et les valeurs de retour, les membres de [**struct**](struct.md) et d' [**Union**](union.md) et d’autres déclarations de type. L’exemple suivant illustre l’utilisation d’un type de données [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) généré automatiquement :

``` syntax
[
    object, 
    uuid (ABCDEFOO-1234-1234-5678-ABCDEF123456)
] 
interface IStream : IUnknown
{ 
    typedef IStream * LPSTREAM; 
    // Other interface definition statements.
}
```

Dans une interface COM, toutes les fonctions membres d’interface sont supposées être des fonctions virtuelles. Une fonction virtuelle a un pointeur **This** implicite en tant que premier paramètre. La table de fonctions virtuelles contient une entrée pour chaque fonction membre d’interface.

Les **\[** [](local.md) **\]** fonctions membres de l’interface d’objet non locale doivent avoir une valeur de retour de HRESULT ou SCODE. (Notez que les versions antérieures de MIDL permettaient aux fonctions membres de retourner [**void**](void.md). Toutefois, à partir de la version 3,0 de MIDL, le retour de **void** génère une erreur du compilateur.) Avoir une valeur de retour HRESULT ou SCODE signifie que si une exception est générée pendant un appel distant, les proxies générés interceptent l’exception et retournent le code d’exception dans la valeur de retour. Si votre application peut se permettre d’ignorer les erreurs qui se produisent pendant un appel de procédure distante, vous pouvez spécifier HRESULT comme type de retour sans vérifier la valeur de retour après l’appel.

Si vous recompilez une ancienne application, la modification des types de retour peut introduire des problèmes de compatibilité descendante lorsque le serveur envoie le résultat nouvellement introduit au client. Comme alternative à la modification du type de retour, vous pouvez étiqueter la fonction qui retourne [**void**](void.md) avec l' **\[** [**appel \_ comme**](call-as.md) attribut, ce qui en **\]** fait une fonction locale. Définissez ensuite une fonction distante associée avec les mêmes paramètres, mais avec le type de retour HRESULT. La fonction locale peut lever une exception en fonction de cette valeur HRESULT, si nécessaire.

L’attribut d' **\[ \] objet** n’est pas disponible quand vous compilez à l’aide du commutateur [**/OSF**](-osf.md) du compilateur MIDL.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    object
] 
interface IMyInterface : IUnknown
{
    // Interface definition statements.
}

[
    uuid(87654321-1234-1234-1234-123456789ABC), 
    object, 
    local
] 
interface ILocalInterface : ISomeOldCOMInterface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**appeler \_ en tant que**](call-as.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**IID \_ est**](iid-is.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**universel**](uuid.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 