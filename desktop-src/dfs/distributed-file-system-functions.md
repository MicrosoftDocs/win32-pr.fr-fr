---
title: Fonctions système de fichiers DFS
description: Les fonctions système de fichiers DFS (DFS) sont les suivantes.
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483768"
---
# <a name="distributed-file-system-functions"></a>Fonctions système de fichiers DFS

Les fonctions système de fichiers DFS (DFS) sont les suivantes.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[NetDfsAdd](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
Crée un nouveau lien système de fichiers DFS (DFS) ou ajoute des cibles à un lien existant dans un espace de noms DFS.

</dd> <dt>

[NetDfsAddFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
Crée un nouvel espace de noms de système de fichiers DFS basé sur un domaine (DFS). Si l’espace de noms existe déjà, la fonction y ajoute la cible racine spécifiée.

</dd> <dt>

[NetDfsAddRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
Crée un espace de noms DFS autonome ou basé sur un domaine ou ajoute une nouvelle cible racine à un espace de noms basé sur un domaine existant.

</dd> <dt>

[NetDfsAddStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
Crée un espace de noms système de fichiers DFS (DFS) autonome.

</dd> <dt>

[NetDfsEnum](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
Énumère les espaces de noms système de fichiers DFS (DFS) hébergés sur un serveur ou les liens DFS d’un espace de noms hébergé par un serveur.

</dd> <dt>

[NetDfsGetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
Récupère des informations sur une racine ou un lien système de fichiers DFS (DFS) à partir du cache conservé par le client DFS.

</dd> <dt>

[NetDfsGetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
Récupère le descripteur de sécurité de l’objet conteneur pour les espaces de noms DFS basés sur un domaine dans le domaine de Active Directory spécifié.

</dd> <dt>

[NetDfsGetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
Récupère des informations sur la racine ou le lien d’un système de fichiers DFS (DFS) spécifié dans un espace de noms DFS.

</dd> <dt>

[NetDfsGetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
Récupère le descripteur de sécurité pour l’objet racine de l’espace de noms DFS spécifié.

</dd> <dt>

[NetDfsGetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
Récupère le descripteur de sécurité pour l’objet conteneur de l’espace de noms DFS autonome spécifié.

</dd> <dt>

[NetDfsGetSupportedNamespaceVersion](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
Détermine le numéro de version des métadonnées prises en charge.

</dd> <dt>

[NetDfsMove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
Renomme ou déplace un lien DFS.

</dd> <dt>

[NetDfsRemove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
Supprime un lien système de fichiers DFS (DFS) ou une cible de lien spécifique d’un lien DFS dans un espace de noms DFS. Lors de la suppression d’une cible de lien spécifique, le lien lui-même est supprimé si la dernière cible de lien du lien est supprimée.

</dd> <dt>

[NetDfsRemoveFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
Supprime la cible racine spécifiée d’un espace de noms de système de fichiers DFS basé sur un domaine (DFS). Si la dernière cible racine de l’espace de noms DFS est supprimée, la fonction supprime également l’espace de noms DFS. Un espace de noms DFS peut être supprimé sans supprimer au préalable tous les liens qu’il contient.

</dd> <dt>

[NetDfsRemoveFtRootForced](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
Supprime la cible racine spécifiée d’un espace de noms de système de fichiers DFS basé sur un domaine (DFS), même si le serveur cible racine est hors connexion. Si la dernière cible racine de l’espace de noms DFS est supprimée, la fonction supprime également l’espace de noms DFS. Un espace de noms DFS peut être supprimé sans supprimer au préalable tous les liens qu’il contient.

> [!Note]
> La fonction [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) ne met pas à jour le registre sur le serveur cible racine DFS. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

[NetDfsRemoveRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
Supprime une cible racine DFS d’un espace de noms DFS basé sur un domaine. Si la cible racine est la dernière cible racine de l’espace de noms DFS, cette fonction supprime l’espace de noms DFS. Cette fonction peut également être utilisée pour supprimer un espace de noms DFS autonome.

</dd> <dt>

[NetDfsRemoveStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
Supprime un espace de noms système de fichiers DFS (DFS) autonome.

</dd> <dt>

[NetDfsSetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
Modifie les informations relatives à une racine ou un lien système de fichiers DFS (DFS) dans le cache géré par le client DFS.

</dd> <dt>

[NetDfsSetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
Définit le descripteur de sécurité de l’objet conteneur pour les espaces de noms DFS basés sur un domaine dans le domaine de Active Directory spécifié.

</dd> <dt>

[NetDfsSetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
Définit ou modifie les informations relatives à une racine système de fichiers DFS (DFS), une cible racine, un lien ou une cible de lien spécifique.

</dd> <dt>

[NetDfsSetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
Définit le descripteur de sécurité pour l’objet racine de l’espace de noms DFS spécifié.

</dd> <dt>

[NetDfsSetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
Définit le descripteur de sécurité pour l’objet conteneur de l’espace de noms DFS autonome spécifié.

</dd> </dl>

Notez qu’une application qui appelle l’une des fonctions peut entraîner indirectement le serveur d’espaces de noms DFS local qui traite l’appel de fonction pour effectuer une synchronisation complète des métadonnées d’espace de noms associées à partir du maître d’émulateur de contrôleur de domaine principal pour ce domaine. Cette synchronisation complète peut se produire même lorsque le mode d’extensibilité racine est configuré pour cet espace de noms.
