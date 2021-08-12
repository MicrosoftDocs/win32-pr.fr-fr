---
description: 'Les structures DFS système de fichiers DFS sont les suivantes :'
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Structures de système de fichiers DFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1561a4586cc03304c6aa1c1e323eb42fd09766df0cc3c7210636367337873a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541280"
---
# <a name="distributed-file-system-structures"></a>Structures de système de fichiers DFS

Les structures système de fichiers DFS (DFS) sont les suivantes :

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

Mémoire tampon d’entrée utilisée avec le code de contrôle [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dd> <dt>

[Structure _DFS_INFO_1](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
Contient le nom d’une racine ou d’un lien système de fichiers DFS (DFS).

</dd> <dt>

[Structure _DFS_INFO_2](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
Contient des informations sur une racine ou un lien système de fichiers DFS (DFS). Cette structure contient le nom, l’État et le nombre de cibles DFS pour la racine ou le lien.

</dd> <dt>

[Structure _DFS_INFO_3](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
Contient des informations sur une racine ou un lien système de fichiers DFS (DFS). Cette structure contient le nom, l’État, le nombre de cibles DFS et des informations sur chaque cible de la racine ou du lien.

</dd> <dt>

[Structure _DFS_INFO_4](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
Contient des informations sur une racine ou un lien système de fichiers DFS (DFS). Cette structure contient le nom, l’État, le **GUID**, le délai d’attente, le nombre de cibles et des informations sur chaque cible de la racine ou du lien.

</dd> <dt>

[Structure _DFS_INFO_5](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
Contient des informations sur une racine ou un lien système de fichiers DFS (DFS). Cette structure contient le nom, l’État, le **GUID**, le délai d’attente, les propriétés d’espace de noms/racine/lien, la taille des métadonnées et le nombre de cibles pour la racine ou le lien.

</dd> <dt>

[Structure _DFS_INFO_6](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
Contient des informations sur une racine ou un lien système de fichiers DFS (DFS). Cette structure contient le nom, l’État, le **GUID**, le délai d’attente, les propriétés d’espace de noms/racine/lien, la taille des métadonnées, le nombre de cibles et les informations sur chaque cible de la racine ou du lien.

</dd> <dt>

[Structure _DFS_INFO_7](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
Contient des informations sur un espace de noms DFS. Cette structure contient le **GUID** de version pour les métadonnées de l’espace de noms.

</dd> <dt>

[Structure _DFS_INFO_8](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
Contient le nom, l’État, le **GUID**, le délai d’attente, les indicateurs de propriété, la taille des métadonnées, les informations cibles DFS et le descripteur de sécurité de point d’analyse de lien pour une racine ou un lien.

</dd> <dt>

[Structure _DFS_INFO_9](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
Contient le nom, l’État, le **GUID**, le délai d’attente, les indicateurs de propriété, la taille des métadonnées, les informations cibles DFS, le descripteur de sécurité du point d’analyse de lien et la liste des cibles DFS pour une racine ou un lien.

</dd> <dt>

[Structure _DFS_INFO_50](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
Contient la version des métadonnées DFS et les fonctionnalités d’un espace de noms DFS existant.

</dd> <dt>

[Structure _DFS_INFO_100](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
Contient un commentaire associé à une racine ou un lien système de fichiers DFS (DFS).

</dd> <dt>

[Structure _DFS_INFO_101](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
Décrit l’état du stockage sur une racine DFS, un lien, une cible racine ou une cible de lien.

</dd> <dt>

[Structure _DFS_INFO_102](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
Contient une valeur de délai d’attente à associer à une racine système de fichiers DFS (DFS) ou à un lien dans une racine DFS nommée.

</dd> <dt>

[Structure _DFS_INFO_103](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
Contient des propriétés qui définissent des comportements spécifiques pour une racine ou un lien DFS.

</dd> <dt>

[Structure _DFS_INFO_104](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
Contient la priorité d’une cible racine DFS ou d’une cible de lien.

</dd> <dt>

[Structure _DFS_INFO_105](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
Contient des informations sur une racine ou un lien DFS, notamment des commentaires, des États, des délais d’attente et des comportements DFS spécifiés par les indicateurs de propriété.

</dd> <dt>

[Structure _DFS_INFO_106](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
Contient l’état de stockage et la priorité d’une cible racine DFS ou d’une cible de lien. Cette structure est uniquement destinée à être utilisée avec la fonction [**NetDfsSetInfo**](netdfssetinfo.md) .

</dd> <dt>

[Structure _DFS_INFO_107](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
Contient des informations sur une racine ou un lien DFS, y compris le commentaire, l’État, le délai d’attente, les indicateurs de propriété et le descripteur de sécurité de point d’analyse de lien.

</dd> <dt>

[Structure _DFS_INFO_150](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
Contient le descripteur de sécurité pour le point d’analyse d’un lien DFS.

</dd> <dt>

[Structure _DFS_INFO_200](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
Contient le nom d’un espace de noms de système de fichiers DFS basé sur un domaine (DFS).

</dd> <dt>

[Structure _DFS_INFO_300](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
Contient le nom et le type (basé sur un domaine ou autonome) d’un espace de noms DFS.

</dd> <dt>

[Structure _DFS_STORAGE_INFO](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
Contient des informations sur une racine DFS ou une cible de lien dans un espace de noms DFS ou à partir du cache géré par le client DFS.

</dd> <dt>

[Structure _DFS_STORAGE_INFO_1](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
Contient des informations sur une cible DFS, y compris le nom du serveur cible DFS et le nom du partage, ainsi que l’État et la priorité de la cible.

</dd> <dt>

[Structure _DFS_SUPPORTED_NAMESPACE_VERSION_INFO](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
Contient les informations de version d’un espace de noms DFS.

</dd> <dt>

[Structure _DFS_TARGET_PRIORITY](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
Contient la classe de priorité et le rang d’une cible DFS spécifique.

</dd> </dl>
