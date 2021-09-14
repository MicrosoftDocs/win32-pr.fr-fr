---
description: La définition d’interface suivante est fournie en tant que norme qui peut être suivie lors du développement d’un fournisseur de services de carte à puce.
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: Interface ISCardFileAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193976"
---
# <a name="iscardfileaccess-interface"></a>Interface ISCardFileAccess

\[L’interface **ISCardFileAccess** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La définition d’interface suivante est fournie en tant que norme qui peut être suivie lors du développement d’un [*fournisseur de services*](../secgloss/c-gly.md)de [*carte à puce*](../secgloss/s-gly.md) .

L’interface **ISCardFileAccess** peut être utilisée pour implémenter une interface de haut niveau sur un système de fichiers à base de cartes avec un système de fichiers de cartes sous-jacent basé sur la structure définie dans la norme ISO/IEC 7816-4. D’autres implémentations sont possibles, mais elles sont supposées être les plus courantes.

L’interface **ISCardFileAccess** peut être utilisée pour exposer des entités de système de fichiers de manière très familière aux développeurs d’applications dans l’environnement de PC. Il fournit des mécanismes pour localiser des fichiers spécifiques et effectuer des opérations courantes, telles que la sélection, la lecture, l’écriture, la création et la suppression. Il encapsule et masque une grande partie des détails de bas niveau liés à l’exécution de ces opérations au niveau de la carte.

Voici une utilisation courante de l’interface **ISCardFileAccess** . Dans ce cas, l’interface **ISCardFileAccess** est utilisée pour sélectionner, ouvrir et écrire dans un fichier.

**Pour écrire dans un fichier**

1.  Appelez [**ISCardManage :: CreateFileAccess**](iscardmanage-createfileaccess.md) pour créer une interface **ISCardFileAccess** .
2.  Appelez [**Open**](iscardfileaccess-open.md) pour sélectionner et ouvrir le fichier.
3.  Appelez [**Write**](iscardfileaccess-write.md).
4.  Appelez [**Close**](iscardfileaccess-close.md).
5.  Libérez l’interface **ISCardFileAccess** .

## <a name="members"></a>Membres

L’interface **ISCardFileAccess** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardFileAccess** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISCardFileAccess** possède ces méthodes.



| Méthode                                                              | Description                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeDir**](iscardfileaccess-changedir.md)                     | Remplace le répertoire de carte à puce actuel par le nouveau répertoire spécifié.<br/>                                                          |
| [**Plus**](iscardfileaccess-close.md)                             | Ferme le fichier spécifié.<br/>                                                                                                        |
| [**Créer**](iscardfileaccess-create.md)                           | Crée un fichier à un emplacement donné dans le système de fichiers ICC.<br/>                                                                    |
| [**Supprimer**](iscardfileaccess-delete.md)                           | Supprime un fichier spécifié.<br/>                                                                                                         |
| [**Répertoire**](iscardfileaccess-directory.md)                     | Récupère une liste de fichiers.<br/>                                                                                                        |
| [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md)             | Retourne un chemin d’accès absolu au répertoire actuellement sélectionné.<br/>                                                                     |
| [**GetFileCapabilities**](iscardfileaccess-getfilecapabilities.md) | Récupère les fonctionnalités de fichier.<br/>                                                                                                      |
| [**GetProperties**](iscardfileaccess-getproperties.md)             | Récupère les données primitives référencées par des balises pour l’objet spécifié.<br/>                                                           |
| [**Invalidate**](iscardfileaccess-invalidate.md)                   | Rend le fichier spécifié non valide.<br/>                                                                                               |
| [**Ouvrir**](iscardfileaccess-open.md)                               | Ouvre le fichier spécifié pour une utilisation ultérieure.<br/>                                                                                         |
| [**En lecture**](iscardfileaccess-read.md)                               | Lit et retourne les données spécifiées à partir d’un fichier donné.<br/>                                                                           |
| [**Réhabiliter**](iscardfileaccess-rehabilitate.md)               | Rend un fichier (EF ou DF) qui a été précédemment rendu non valide à l’aide de la commande Invalidate, accessible par l’application.<br/> |
| [**Seek**](iscardfileaccess-seek.md)                               | Sélectionne l’objet à partir duquel l’autorisation de lecture/écriture sera effectuée.<br/>                                                                 |
| [**SetProperties**](iscardfileaccess-setproperties.md)             | Définit les données primitives référencées par des balises pour l’objet spécifié.<br/>                                                                |
| [**Write**](iscardfileaccess-write.md)                             | Écrit des données dans un fichier ouvert en cours.<br/>                                                                                             |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



 

 
