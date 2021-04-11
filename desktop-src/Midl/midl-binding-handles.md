---
title: Handles de liaison MIDL
description: Les handles de liaison sont des objets de données qui représentent la liaison entre le client et le serveur.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- types de données MIDL, handles de liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031072"
---
# <a name="midl-binding-handles"></a>Handles de liaison MIDL

Les handles de liaison sont des objets de données qui représentent la liaison entre le client et le serveur.

MIDL prend en charge le [**handle \_**](handle-t.md)de type de base t. Les handles de ce type sont appelés « Handles primitifs ».

Vous pouvez définir vos propres types de handles à l’aide de l’attribut **\[ descripteur \]** . Les handles définis de cette façon sont appelés Handles « définis par l’utilisateur » ou « personnalisés » ou « génériques ».

Vous pouvez également définir un handle qui gère les informations d’État à l’aide de l’attribut de **\[** [**\_ handle de contexte**](context-handle.md) **\]** . Les handles définis de cette façon sont appelés Handles « Context ».

Si aucune information d’État n’est nécessaire et que vous ne choisissez pas d’appeler les bibliothèques Runtime RPC pour gérer le handle, vous pouvez demander que les bibliothèques Runtime fournissent une liaison automatique. Pour ce faire, utilisez le **\[** [**\_ descripteur automatique**](auto-handle.md)de mot clé ACF **\]** .

Vous pouvez spécifier une variable globale comme handle de liaison à l’aide du mot clé ACF **\[** [**\_ handle implicite**](implicit-handle.md) **\]** . Le mot clé **\[ \_ handle \] explicite** est utilisé pour indiquer que chaque fonction distante a un handle explicitement spécifié.

Pour plus d’informations, consultez [liaison et Handles](/windows/desktop/Rpc/binding-and-handles).

 

 