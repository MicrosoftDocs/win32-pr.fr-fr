---
description: HKLM \\ Software \\ Microsoft \\ MSSQLSERVER \\ client.
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637a77589d211aae6eb51cacd6376d86367175699b7a339f11f19cc2108b80e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084739"
---
# <a name="connectto"></a>ConnectTo

**HKLM \\ Software \\ Microsoft \\ MSSQLSERVER \\ client**

## <a name="description"></a>Description

la sous-clé **ConnectTo** stocke les informations de connexion pour les clients Windows qui se connectent aux instances du moteur de base de données Microsoft SQL Server. Les entrées de registre de cette sous-clé sont du type de données « REG \_ SZ » et leurs valeurs spécifient les Net-Library à utiliser pour se connecter à l’instance, ainsi que tous les paramètres spécifiques au réseau.

les informations de connexion stockées dans cette sous-clé sont lues par le fournisseur de OLE DB pour SQL Server, le pilote ODBC SQL Server ou la SQL Server DB-Library bibliothèque de liens dynamiques (DLL).

## <a name="change-method"></a>Modifier la méthode

Vous ne devez pas modifier les entrées de cette sous-clé à l’aide de l’éditeur du Registre. utilisez l’utilitaire réseau du Client SQL Server pour configurer le nom du serveur et les informations de connexion. pour obtenir des instructions supplémentaires, consultez SQL Server l’aide de l’utilitaire réseau Client.

## <a name="notes"></a>Notes

-   la sous-clé **ConnectTo** est utilisée par le fournisseur de OLE DB pour SQL Server, le pilote ODBC SQL Server et le SQL Server DLL DB-Library. Les entrées de cette sous-clé identifient les Net-Library ces composants de l’interface de programmation d’applications (API) d’accès aux données appellent.
-   Net-Libraries sont des composants SQL Server qui protègent les composants de l’API d’accès aux données des détails de l’utilisation de différentes méthodes de communication interprocessus (IPC) pour communiquer avec une instance du moteur de base de données SQL Server.
-   une mise à jour incorrecte de la sous-clé **ConnectTo** peut empêcher les applications de se connecter à une instance du moteur de base de données SQL Server.

 

 



