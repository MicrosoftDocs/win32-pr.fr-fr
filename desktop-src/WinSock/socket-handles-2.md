---
description: un handle de socket peut éventuellement être un descripteur de fichier dans Windows sockets 2. Un descripteur de socket d’un fournisseur Winsock peut être utilisé avec d’autres fonctions non-Winsock, telles que ReadFile, WriteFile, ReadFileEx et WriteFileEx.
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: Handles de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91a9c9c642c317e9ab4ef897a20b68184df2c04324bcb76c33dea762e78c2846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740033"
---
# <a name="socket-handles"></a>Handles de socket

un handle de socket peut éventuellement être un descripteur de fichier dans Windows sockets 2. Un descripteur de socket d’un fournisseur Winsock peut être utilisé avec d’autres fonctions non-Winsock, telles que [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)et [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex).

Le membre **XP1 \_ IFS \_ gère** la structure d’informations de protocole pour un fournisseur détermine si un handle de socket d’un fournisseur est un handle IFS (Installable File System). Les descripteurs de socket qui sont des handles IFS peuvent être utilisés sans aucune altération des performances avec d’autres fonctions non-Winsock ([**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) et [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), par exemple). Les descripteurs de socket non-IFS lorsqu’ils sont utilisés avec des fonctions non-Winsock (**ReadFile** et **WriteFile**, par exemple) entraînent des interactions entre le fournisseur et le système de fichiers où une surcharge de traitement supplémentaire est impliquée, ce qui peut entraîner une baisse significative des performances. Lorsque vous utilisez des descripteurs de socket avec des fonctions non-Winsock, les codes d’erreur propagés à partir du système de fichiers de base ne sont pas toujours mappés aux codes d’erreur Winsock. Par conséquent, il est recommandé d’utiliser les descripteurs de socket uniquement avec les fonctions Winsock.

Un descripteur de socket ne doit pas être utilisé avec la fonction [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) . La présence de fournisseurs de services en couche (LSP) peut provoquer l’échec de cette opération et il n’existe aucun moyen pour le processus de destination d’importer le descripteur de Socket.

> [!Note]  
> Les fournisseurs de services en couche sont déconseillés. à partir de Windows 8 et Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).

 

Windows Sockets 2 a développé certaines fonctions qui transfèrent les données entre les sockets à l’aide de handles. Les fonctions offrent des avantages spécifiques aux sockets pour transférer des données et incluent [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)et [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa).

 

 
