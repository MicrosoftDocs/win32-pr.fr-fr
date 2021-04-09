---
description: HKLM \\ Software \\ Microsoft \\ MSSQLSERVER \\ client.
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033657"
---
# <a name="connectto"></a>ConnectTo

**HKLM \\ Software \\ Microsoft \\ MSSQLSERVER \\ client**

## <a name="description"></a>Description

La sous-clé **ConnectTo** stocke les informations de connexion pour les clients Windows qui se connectent aux instances du moteur de base de données Microsoft SQL Server. Les entrées de registre de cette sous-clé sont du type de données « REG \_ SZ » et leurs valeurs spécifient les Net-Library à utiliser pour se connecter à l’instance, ainsi que tous les paramètres spécifiques au réseau.

Les informations de connexion stockées dans cette sous-clé sont lues par le fournisseur de OLE DB pour SQL Server, le pilote ODBC SQL Server ou la SQL Server DB-Library bibliothèque de liens dynamiques (DLL).

## <a name="change-method"></a>Modifier la méthode

Vous ne devez pas modifier les entrées de cette sous-clé à l’aide de l’éditeur du Registre. Utilisez l’utilitaire réseau du client SQL Server pour configurer le nom du serveur et les informations de connexion. Pour obtenir des instructions supplémentaires, consultez SQL Server l’aide de l’utilitaire réseau client.

## <a name="notes"></a>Notes

-   La sous-clé **ConnectTo** est utilisée par le fournisseur de OLE DB pour SQL Server, le pilote ODBC SQL Server et le SQL Server dll DB-Library. Les entrées de cette sous-clé identifient les Net-Library ces composants de l’interface de programmation d’applications (API) d’accès aux données appellent.
-   Net-Libraries sont des composants SQL Server qui protègent les composants de l’API d’accès aux données des détails de l’utilisation de différentes méthodes de communication interprocessus (IPC) pour communiquer avec une instance du moteur de base de données SQL Server.
-   Une mise à jour incorrecte de la sous-clé **ConnectTo** peut empêcher les applications de se connecter à une instance du moteur de base de données SQL Server.

 

 



