---
title: IRootStorage-implémentation de fichier composé
description: L’implémentation de fichier composé de COM de IRootStorage vous permet de prendre en charge l’enregistrement de fichiers en cas de mémoire insuffisante ou d’espace disque faible. Pour plus d’informations sur le comportement de cette interface, consultez IRootStorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd STG, implémentation de fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20128e749443d19c6418703bf64d93eb763ae25103d677719bb4cb4cd21349a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961197"
---
# <a name="irootstorage---compound-file-implementation"></a>IRootStorage-implémentation de fichier composé

L’implémentation de fichier composé de COM de [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) vous permet de prendre en charge l’enregistrement de fichiers en cas de mémoire insuffisante ou d’espace disque faible. Pour plus d’informations sur le comportement de cette interface, consultez **IRootStorage**.

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez l’implémentation fournie par le système de [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) uniquement pour prendre en charge l’enregistrement de fichiers dans des conditions de mémoire insuffisante.

## <a name="remarks"></a>Remarques

Il est possible d’appeler l’implémentation COM de [**IRootStorage :: SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) pour effectuer une opération Enregistrer sous normale dans un autre fichier. Toutefois, les applications qui le font peuvent ne pas être compatibles avec les futures générations de stockage COM. Pour éviter cette éventualité, les applications effectuant une opération Enregistrer sous doivent créer manuellement le deuxième fichier composé et appeler [**IStorage :: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto). La méthode **IRootStorage :: SwitchToFile** doit être utilisée uniquement dans les situations d’urgence (mémoire insuffisante ou espace disque).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




