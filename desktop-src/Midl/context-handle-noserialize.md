---
title: attribut context_handle_noserialize
description: L’attribut \ de handle de contexte \_ \_ noserialize \ ACF garantit qu’un handle de contexte ne sera jamais sérialisé, quel que soit le comportement par défaut de l’application.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize MIDL de l’attribut
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f3f2a72837df5efa3b74bd2672e39c3c3b12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724964"
---
# <a name="context_handle_noserialize-attribute"></a>\_attribut noserialize de handle de contexte \_

L’attribut de **\[ Gestionnaire de contexte \_ \_ noserialize \]** , qui garantit qu’un handle de contexte ne sera jamais sérialisé, quel que soit le comportement par défaut de l’application.

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type-ACF-attribute-List* 
</dt> <dd>

Tous les autres attributs ACF qui s’appliquent au type.

</dd> <dt>

*Context-handle-type* 
</dt> <dd>

Identificateur qui spécifie le type de handle de contexte, tel que défini dans une déclaration [**typedef**](typedef.md) . Il s’agit du type qui reçoit l’attribut de [**\[ \_ handle \] de contexte**](context-handle.md) dans le fichier IDL.

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

L’attribut de [**\[ \_ handle \] de contexte**](context-handle.md) identifie un handle de liaison qui gère le contexte, ou les informations d’État, sur le serveur entre les appels de procédure distante. L’attribut peut apparaître en tant qu’attribut de type [**typedef**](typedef.md) IDL, en tant qu’attribut de type de retour de fonction ou en tant qu’attribut de paramètre.

Par défaut, les appels sur les handles de contexte sont sérialisés. Une application peut appeler [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) pour remplacer ce comportement par défaut. L’utilisation de l’attribut [**\[ \_ handle \] de contexte**](context-handle.md) dans un fichier ACF garantit que les appels sur ce handle de contexte particulier ne seront pas sérialisés, quel que soit le comportement de l’application appelante. La fourniture d’une routine d’arrêt de contexte est facultative.

Cet attribut est disponible dans MIDL version 5,0.

**Windows ServerÂ 2003 et WINDOWSÂ XP ou version ultérieure :** Une interface unique peut prendre en charge des handles de contexte sérialisés et non sérialisés, ce qui permet à une méthode sur une interface d’accéder exclusivement à un handle de contexte (sérialisé), tandis que d’autres méthodes accèdent à ce handle de contexte en mode partagé (non sérialisé). Ces fonctionnalités d’accès sont comparables aux mécanismes de verrouillage en lecture/écriture. les méthodes qui utilisent un handle de contexte sérialisé sont des utilisateurs exclusifs (enregistreurs), tandis que les méthodes qui utilisent un handle de contexte non sérialisé sont des utilisateurs partagés (lecteurs). Les méthodes qui détruisent ou modifient l’état d’un handle de contexte doivent être sérialisées. Les méthodes qui ne modifient pas l’état d’un handle de contexte, telles que les méthodes qui lisent simplement un handle de contexte, peuvent être non sérialisées. Notez que les méthodes de création sont implicitement sérialisées.

## <a name="examples"></a>Exemples

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs ACF](acf-attributes.md)
</dt> <dt>

[**\_sérialisation du handle de contexte \_**](context-handle-serialize.md)
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

 

 