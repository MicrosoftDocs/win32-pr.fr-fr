---
title: attribut context_handle_serialize
description: L’attribut \ Context \_ handle \_ Serialize \ ACF garantit qu’un handle de contexte sera toujours sérialisé, quel que soit le comportement par défaut de l’application.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize MIDL de l’attribut
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106543046"
---
# <a name="context_handle_serialize-attribute"></a>attribut de sérialisation du \_ handle de contexte \_

L’attribut de **\[ handle de contexte de \_ \_ sérialisation \] de contexte** garantit qu’un handle de contexte sera toujours sérialisé, quel que soit le comportement par défaut de l’application.

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type-ACF-attribute-List* 
</dt> <dd>

Tous les autres attributs ACF qui s’appliquent au type.

</dd> <dt>

*Context-handle-type* 
</dt> <dd>

Identificateur qui spécifie le type de handle de contexte, tel que défini dans une déclaration [**typedef**](typedef.md) . Il s’agit du type qui reçoit l’attribut de **\[ \_ \_ sérialisation \] du handle de contexte** dans le fichier IDL.

</dd> <dt>

*function-ACF-attribute-List* 
</dt> <dd>

Tous les attributs ACF supplémentaires qui s’appliquent à la fonction.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Nom de la fonction tel qu’il est défini dans le fichier IDL.

</dd> <dt>

*Parameter-ACF-attribute-List* 
</dt> <dd>

Tous les autres attributs ACF qui s’appliquent au paramètre.

</dd> <dt>

*nom du paramètre* 
</dt> <dd>

Nom du paramètre tel que défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut de **\[ \_ \_ sérialisation \] du handle de contexte** identifie un handle de liaison qui gère les informations de contexte ou d’État sur le serveur entre les appels de procédure distante. L’attribut peut apparaître en tant qu’attribut de type [**typedef**](typedef.md) IDL, en tant qu’attribut de type de retour de fonction ou en tant qu’attribut de paramètre.

Par défaut, les appels sur les handles de contexte sont sérialisés, mais une application peut appeler [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) pour remplacer ce comportement par défaut. L’utilisation de l’attribut de **\[ \_ \_ sérialisation \] du handle de contexte** dans un fichier ACF garantit que les appels sur ce handle de contexte particulier seront sérialisés, même si l’application appelante a remplacé la sérialisation par défaut. Une routine d’arrêt de contexte est facultative.

Cet attribut est disponible dans MIDL version 5,0.

**Windows ServerÂ 2003 et WINDOWSÂ XP ou version ultérieure :** Une interface unique peut prendre en charge des handles de contexte sérialisés et non sérialisés, ce qui permet à une méthode sur une interface d’accéder exclusivement à un handle de contexte (sérialisé), tandis que d’autres méthodes accèdent à ce handle de contexte en mode partagé (non sérialisé). Ces fonctionnalités d’accès sont comparables aux mécanismes de verrouillage en lecture/écriture. les méthodes qui utilisent un handle de contexte sérialisé sont des utilisateurs exclusifs (enregistreurs), tandis que les méthodes qui utilisent un handle de contexte non sérialisé sont des utilisateurs partagés (lecteurs). Les méthodes qui détruisent ou modifient l’état d’un handle de contexte doivent être sérialisées. Les méthodes qui ne modifient pas l’état d’un handle de contexte, telles que les méthodes qui lisent simplement un handle de contexte, peuvent être non sérialisées. Notez que les méthodes de création sont implicitement sérialisées.

## <a name="examples"></a>Exemples

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Attributs ACF](acf-attributes.md)
</dt> <dt>

[**handle de contexte \_ \_ noserialize**](context-handle-noserialize.md)
</dt> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[Handles de contexte](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[Routine d’exécution du contexte de serveur](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[Clients multithread et handles de contexte](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 