---
title: Gestionnaire de documents
description: Gestionnaire de documents
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- Text Services Framework (TSF), gestionnaire de documents
- TSF (Text Services Framework), gestionnaire de documents
- services de texte, gestionnaire de documents
- Applications compatibles TSF, gestionnaire de documents
- Gestionnaire de documents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672142"
---
# <a name="document-manager"></a>Gestionnaire de documents

## <a name="applications"></a>Applications

Pour créer un objet du gestionnaire de documents, une application appelle [ITfThreadMgr :: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr). L’application crée un objet de gestionnaire de documents distinct pour chaque document individuel géré par l’application. L’application utilise le gestionnaire de documents pour créer des contextes de modification, ajouter un contexte à la pile de contexte et supprimer un contexte de la pile de contexte.

## <a name="text-services"></a>Services de texte

Un service de texte ne crée jamais un objet de gestionnaire de documents. Au lieu de cela, le service de texte obtient l’objet actuellement actif du gestionnaire de documents en appelant [ITfThreadMgr :: getFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus). Un service de texte utilise le gestionnaire de documents pour obtenir le contexte en haut de la pile.

Un service de texte peut également utiliser le gestionnaire de documents pour créer son propre contexte et l’ajouter et le supprimer de la pile de contexte. Cela s’effectue normalement lorsque le service de texte doit afficher une interface utilisateur modale, par exemple lorsqu’une liste de mots est affichée pour permettre à l’utilisateur de sélectionner un mot. Lorsque la liste est affichée, le service de texte place son propre contexte sur la pile. Quand la liste de mots est fermée, le service de texte supprime son contexte de la pile.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr :: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[ITfThreadMgr :: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




