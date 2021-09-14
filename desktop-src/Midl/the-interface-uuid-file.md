---
title: Fichier UUID de l’interface
description: Le fichier UUID de l’interface collecte les définitions des identificateurs d’interface à partir de toutes les interfaces dans le fichier IDL traité.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL et COM MIDL, interfaces, fichiers UUID de proxy
- MIDL du fichier UUID de l’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093125"
---
# <a name="the-interface-uuid-file"></a>Fichier UUID de l’interface

Le fichier UUID de l’interface collecte les définitions des identificateurs d’interface à partir de toutes les interfaces dans le fichier IDL traité. À l’instar du fichier stub et du fichier d’en-tête, la fermeture du flux d’entrée est définie par le fichier IDL actuel et les fichiers inclus. Par exemple, pour l’interface IFace, le compilateur génère une IFace IID constante \_ et l’initialise à l’UUID de l’interface spécifié dans le fichier IDL. Les applications clientes et la DLL de proxy utilisent cette constante pour identifier l’interface.

Le nom par défaut d’un fichier d’IID d’interface généré à partir d’un fichier. idl est file \_ i.c. Le commutateur du compilateur [**/IID**](-iid.md) MIDL remplace le nom par défaut du fichier UUID de l’interface.

 

 




