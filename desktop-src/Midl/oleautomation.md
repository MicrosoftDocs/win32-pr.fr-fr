---
title: oleautomation (attribut)
description: Attribut de MIDL oleautomation et compatibilité avec Automation.
ms.assetid: 4a1c9a02-d637-4595-87b3-5fe903149357
keywords:
- attribut oleautomation MIDL
topic_type:
- apiref
api_name:
- oleautomation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827aba4cb0871f7130e658299c6d8836557a156
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031221"
---
# <a name="oleautomation-attribute"></a>oleautomation (attribut)

L’attribut **oleautomation** indique qu’une interface est compatible avec Automation.

``` syntax
[ 
    oleautomation, 
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

Spécifie une chaîne UUID générée par l’utilitaire uuidgen.

</dd> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie d’autres attributs qui s’appliquent à l’ensemble de l’interface.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*interface de base* 
</dt> <dd>

Spécifie le nom d’une interface Automation à partir de laquelle cette interface dérivée hérite des fonctions membres, des codes d’État et des attributs d’interface. Toutes les interfaces d’automatisation sont dérivées de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ou [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

</dd> </dl>

## <a name="remarks"></a>Notes

Les paramètres et les types de retour spécifiés pour les membres d’une interface **\[ oleautomation \]** doivent être compatibles Automation, comme indiqué dans le tableau suivant.



| Type                                            | Description                                                                                                                                                                                                   |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **boolean**                                     | Élément de données qui peut avoir la valeur VARIANT \_ true ou variant \_ false. La taille correspond à VARIANT \_ bool.                                                                                                     |
| **unsigned char**                               | élément de données non signées 8 bits.                                                                                                                                                                                     |
| **double**                                      | nombre à virgule flottante IEEE 64 bits.                                                                                                                                                                            |
| **float**                                       | nombre à virgule flottante IEEE 32 bits.                                                                                                                                                                            |
| **int**                                         | Entier signé dont la taille dépend du système. Sur les plateformes 32 bits, MIDL traite [**int**](int.md) comme un entier signé 32 bits.                                                                               |
| **long**                                        | Entier signé 32 bits.                                                                                                                                                                                        |
| **short**                                       | entier signé 16 bits.                                                                                                                                                                                        |
| **BSTR**                                        | Chaîne préfixée par sa longueur, comme décrit dans la rubrique d’automatisation [BSTR](/previous-versions/windows/desktop/automat/bstr).                                                                                                    |
| **CURRENCY**                                    | nombre à virgule flottante fixe sur 8 octets.                                                                                                                                                                          |
| **DATE**                                        | 64 bits, nombre de jours fractionnaires à virgule flottante depuis le 30 décembre 1899.                                                                                                                                     |
| **SCODE**                                       | Pour les systèmes 16 bits : type d’erreur intégré qui correspond à l' \_ erreur VT.                                                                                                                                         |
| **Enum typedef** Â  *MyEnum*                      | Entier signé dont la taille dépend du système.                                                                                                                                                               |
| **Interface IDispatch \***                      | Pointeur vers l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ( \_ Dispatch VT).                                                                                                                |
| **Interface IUnknown \***                       | Pointeur vers une interface qui ne dérive pas de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ inconnu). (Toute interface OLE peut être représentée par son interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .) |
| **dispinterface** Â  *TypeName \**                | Pointeur vers une interface dérivée de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ( \_ distribution vt).                                                                                                    |
| **Coclasse** Â  *TypeName \**                      | Pointeur vers un nom de coclasse (VT \_ inconnu).                                                                                                                                                                      |
| **\[ oleautomation, \] interface** Â   *TypeName \** | Pointeur vers une interface qui dérive de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).                                                                                                                                      |
| **SAFEARRAY**(*TypeName*)                       | *TypeName* est l’un des types ci-dessus. Tableau de ces types.                                                                                                                                                   |
| **TypeName \***                                 | *TypeName* est l’un des types ci-dessus. Pointeur vers un type.                                                                                                                                                      |
| **Décimal**                                     | entier binaire non signé 96 bits mis à l’échelle par une puissance variable de 10. Type de données décimal qui fournit une taille et une échelle pour un nombre (comme en coordonnées).                                                       |



 

Un paramètre est compatible avec Automation si son type est un type compatible Automation, un pointeur vers un type compatible Automation ou un SAFEARRAY d’un type compatible Automation.

Un type de retour est compatible avec Automation si son type est un HRESULT, SCODE ou [**void**](void.md). Toutefois, MIDL requiert que les méthodes d’interface retournent HRESULT ou SCODE. Le retour de **void** génère une erreur du compilateur.

Un membre est compatible avec Automation si son type de retour et tous ses paramètres sont compatibles avec Automation.

Une interface est compatible avec l’Automation si elle est dérivée de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ou [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), elle a l’attribut **\[ OLEAUTOMATION \]** , et toutes ses entrées VTBL sont compatibles Automation. Pour les plateformes 32 bits, la Convention d’appel pour toutes les méthodes dans l’interface doit être STDCALL. Pour les systèmes 16 bits, toutes les méthodes doivent avoir la Convention d’appel CDECL.

Chaque [**dispinterface**](dispinterface.md) est implicitement compatible avec Automation. Par conséquent, vous ne devez pas utiliser l’attribut **\[ \] oleautomation** sur **dispinterface**.

L’attribut **\[ \] oleautomation** n’est pas disponible quand vous compilez à l’aide du commutateur [**/OSF**](-osf.md) du compilateur MIDL.

### <a name="flags"></a>Indicateurs

TYPEFLAG \_ FOLEAUTOMATION

## <a name="examples"></a>Exemples

``` syntax
library Hello
{
    importlib("stdole32.tlb");
    [
        uuid(12345678-1234-1234-1234-123456789ABC),
        helpstring("Application object for the Hello application."),
        oleautomation,
        dual
    ]
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }

    // Other library definition statements.
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**universel**](uuid.md)
</dt> </dl>

 

 