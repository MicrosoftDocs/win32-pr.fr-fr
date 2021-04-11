---
title: Microsoft Interface Definition Language
description: Le Microsoft Interface Definition Language (MIDL) définit des interfaces entre les programmes client et serveur.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL, (voir Microsoft Interface Definition Language MIDL)
- Microsoft Interface Definition Language MIDL
- Microsoft Interface Definition Language MIDL, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e274d66ae234205f5db1f41b2d191ea409561bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031137"
---
# <a name="microsoft-interface-definition-language"></a>Microsoft Interface Definition Language

## <a name="purpose"></a>Objectif

Le Microsoft Interface Definition Language (MIDL) définit des interfaces entre les programmes client et serveur. Microsoft comprend le compilateur MIDL avec le kit de développement logiciel (SDK) de la plateforme pour permettre aux développeurs de créer les fichiers IDL (Interface Definition Language) et les fichiers de configuration d’application (ACF) requis pour les interfaces RPC (Remote Procedure Call) et les interfaces COM/DCOM. MIDL prend également en charge la génération de bibliothèques de types pour OLE Automation.

## <a name="where-applicable"></a>Le cas échéant

MIDL peut être utilisé dans toutes les applications client/serveur basées sur les systèmes d’exploitation Windows. Il peut également être utilisé pour créer des programmes client et serveur pour les environnements réseau hétérogènes qui incluent des systèmes d’exploitation tels que UNIX et Apple. Microsoft prend en charge la norme DCE Open Group (anciennement Open Software Foundation) pour l’interopérabilité RPC.

## <a name="developer-audience"></a>Développeurs concernés

Lors de l’utilisation de MIDL avec RPC, vous devez vous familiariser avec la programmation C/C++ et le paradigme RPC. Lors de l’utilisation de MIDL avec COM, vous devez vous familiariser avec la programmation C++ et le paradigme RPC tel qu’il s’applique à COM. vous pouvez également vous familiariser avec les bibliothèques de types et de scripts de modèle OLE Automation.

## <a name="run-time-requirements"></a>Conditions d’exécution

Les bibliothèques Runtime appropriées pour l’utilisation de MIDL sont fournies avec Windows. Le compilateur MIDL et les composants de l’environnement de développement RPC sont installés lorsque vous installez le SDK Windows. Pour plus d’informations, consultez [utilisation du compilateur MIDL](using-the-midl-compiler-2.md) et [installation de l’environnement de programmation RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                               | Description                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Vue d'ensemble](about-this-guide-2.md)<br/>                                                       | Informations générales sur MIDL et le compilateur MIDL.<br/>                   |
| [Utilisation du compilateur MIDL](using-the-midl-compiler-2.md)<br/>                                 | Informations sur l’utilisation du compilateur prend MIDL pour générer des stubs RPC.<br/>       |
| [Définitions d’interface et bibliothèques de types](interface-definitions-and-type-libraries.md)<br/> | Documentation des définitions d’interface spécifiques à RPC et des bibliothèques de types.<br/> |
| [Référence de Command-Line MIDL](midl-command-line-reference.md)<br/>                           | Documentation des commutateurs de ligne de commande du compilateur MIDL.<br/>               |
| [Référence du langage MIDL](midl-language-reference.md)<br/>                                   | Référence du langage du compilateur MIDL.<br/>                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appel de procédure distante (RPC)](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

