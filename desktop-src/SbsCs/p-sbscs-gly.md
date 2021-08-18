---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (applications isolées et assemblys côte à côte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc8e3d2591cfa1544ce11045f95df42e4a27d39b4a2b40d09bc3f2c907c2abec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142012"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a>P (applications isolées et assemblys côte à côte)

[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) e F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**configuration par application**
</dt> <dd>

Configuration qui peut remplacer la configuration d’application globale d’un assembly spécifique. Une configuration par application est spécifiée par un fichier manifeste de configuration de l’application installé dans le même dossier que le fichier exécutable. Le fichier manifeste décrit la version, ou la plage de versions, des assemblys côte à côte devant être utilisés par l’application. La configuration par application peut être utilisée quand une nouvelle version d’un assembly est incompatible avec une application. Dans ce cas, la configuration globale ou par défaut de l’application peut être remplacée pour un assembly côte à côte spécifique.

</dd> <dt>

<span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly côte à côte privé**
</dt> <dd>

Un assembly côte à côte privé est uniquement visible pour une application spécifiée. Il est installé localement dans une application isolée et le code de l’assembly devient privé dans le contexte de l’application. Les dépendances d’un assembly côte à côte privé sont décrites dans le fichier manifeste de l’application. Les assemblys côte à côte privés peuvent être utilisés pour décaler les effets négatifs du partage d’assembly, tels que les conflits de DLL, et pour faciliter le déploiement d’applications.

</dd> <dt>

<span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**jeton de clé publique**
</dt> <dd>

Chaîne hexadécimale de 16 caractères qui représente les 8 derniers octets du hachage SHA-1 de la clé publique sous laquelle l’assembly est signé. La clé publique utilisée pour signer le catalogue doit être supérieure ou égale à 2048 bits. Obligatoire pour tous les assemblys côte à côte partagés.

</dd> </dl>

 

 



