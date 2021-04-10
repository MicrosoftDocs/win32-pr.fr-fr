---
title: IRootStorage-implémentation de fichier composé
description: L’implémentation de fichier composé de COM de IRootStorage vous permet de prendre en charge l’enregistrement de fichiers en cas de mémoire insuffisante ou d’espace disque faible. Pour plus d’informations sur le comportement de cette interface, consultez IRootStorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd STG, implémentation de fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675913"
---
# <a name="irootstorage---compound-file-implementation"></a>IRootStorage-implémentation de fichier composé

L’implémentation de fichier composé de COM de [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) vous permet de prendre en charge l’enregistrement de fichiers en cas de mémoire insuffisante ou d’espace disque faible. Pour plus d’informations sur le comportement de cette interface, consultez **IRootStorage**.

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez l’implémentation fournie par le système de [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) uniquement pour prendre en charge l’enregistrement de fichiers dans des conditions de mémoire insuffisante.

## <a name="remarks"></a>Notes

Il est possible d’appeler l’implémentation COM de [**IRootStorage :: SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) pour effectuer une opération Enregistrer sous normale dans un autre fichier. Toutefois, les applications qui le font peuvent ne pas être compatibles avec les futures générations de stockage COM. Pour éviter cette éventualité, les applications effectuant une opération Enregistrer sous doivent créer manuellement le deuxième fichier composé et appeler [**IStorage :: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto). La méthode **IRootStorage :: SwitchToFile** doit être utilisée uniquement dans les situations d’urgence (mémoire insuffisante ou espace disque).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




