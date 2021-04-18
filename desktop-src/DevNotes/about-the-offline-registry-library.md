---
description: La bibliothèque de Registre hors connexion est utilisée pour modifier une ruche de registre en dehors du Registre système actif.
ms.assetid: 61db2804-1b67-473f-8dd7-6be6c6a7184e
title: À propos de la bibliothèque de Registre hors connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e08b401a4a77f55a54c48ad147bf38c8796472
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482856"
---
# <a name="about-the-offline-registry-library"></a>À propos de la bibliothèque de Registre hors connexion

La bibliothèque de Registre hors connexion est utilisée pour modifier une ruche de registre en dehors du Registre système actif.

La bibliothèque de Registre hors connexion est conçue pour les scénarios de mise à jour du Registre, tels que la maintenance d’une image de système d’exploitation. Les fonctions de Registre hors connexion offrent les fonctionnalités suivantes qui ne sont pas disponibles avec les fonctions de Registre standard :

-   Les fonctions de Registre hors connexion peuvent être utilisées pour modifier une ruche de Registre dans n’importe quel format de Registre pris en charge. Les fonctions de Registre standard peuvent apporter des modifications uniquement à une ruche de Registre active et les modifications doivent être compatibles avec la version de Windows exécutée sur le système.
-   La bibliothèque de Registre hors connexion requiert uniquement un accès en lecture pour ouvrir un fichier ruche du Registre et un accès en écriture pour enregistrer le fichier. Aucune autre vérification d’accès n’est effectuée sur les objets dans Hive, ce qui permet de modifier la ruche avec des privilèges d’utilisateur standard. Avec les fonctions de Registre standard, le chargement d’une ruche dans le Registre actif est une opération privilégiée qui nécessite un accès administratif.

Les fonctions de Registre hors connexion ne doivent pas être utilisées comme substituts pour les fonctions de Registre système pour les raisons suivantes :

-   Il est impossible de partager les ruches de Registre entre les processus à l’aide des fonctions de Registre hors connexion.
-   Les fonctions de Registre hors connexion utilisent un verrouillage simple qui peut entraîner une dégradation sérieuse des performances pour les applications multithread.
-   Les modifications apportées avec les fonctions de Registre hors connexion ne sont pas enregistrées tant que la fonction [**ORSaveHive**](orsavehive.md) n’est pas appelée.

Les applications ne doivent pas utiliser les fonctions de Registre hors connexion pour contourner les exigences de sécurité du Registre système. Pour charger une ruche, une application qui s’exécute sans les privilèges spéciaux requis par la fonction [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) peut utiliser la fonction [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) .

**Windows Server 2003 et Windows XP :** La fonction [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) n’est pas prise en charge.

Une *ruche de Registre hors connexion* est une ruche de Registre qui a été chargée en mémoire à l’aide des fonctions de Registre hors connexion. Pour créer une ruche de Registre hors connexion vide, utilisez la fonction [**ORCreateHive**](orcreatehive.md) . Pour modifier une ruche de Registre existante, utilisez la fonction [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) ou [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) pour enregistrer une ruche du Registre système actif dans un fichier, puis utilisez la fonction [**OROpenHive**](oropenhive.md) pour ouvrir le fichier.

Les fonctions [**ORCreateHive**](orcreatehive.md) et [**OROpenHive**](oropenhive.md) retournent un handle vers la clé racine de la ruche de Registre hors connexion. Ce descripteur peut être utilisé comme un descripteur d’une autre clé de la ruche de Registre hors connexion, avec les exceptions suivantes : les fonctions [**ORCreateKey**](orcreatekey.md) et [**OROpenKey**](oropenkey.md) ne peuvent pas être utilisées pour retourner un handle à la clé racine ; la fonction [**ORCloseKey**](orclosekey.md) ne peut pas être utilisée pour fermer la clé racine ; et la fonction [**ORDeleteKey**](ordeletekey.md) ne peut pas être utilisée pour supprimer la clé racine. Dans tous ces cas, la fonction échoue avec un **\_ \_ paramètre d’erreur non valide**.

Utilisez la fonction [**ORCreateKey**](orcreatekey.md) pour ajouter des clés à une ruche de Registre ouverte en mode hors connexion et la fonction [**ORSetValue**](orsetvalue.md) pour définir les valeurs des clés. La bibliothèque de Registre hors connexion prend en charge d’autres opérations de registre de base, telles que l’énumération, la récupération et la suppression de clés et de valeurs, ainsi que la définition d’attributs clés tels que la sécurité et le comportement de virtualisation. Pour obtenir la liste des fonctions, consultez fonctions de la [bibliothèque de Registre hors connexion](offline-registry-library-functions.md).

Pour enregistrer les modifications apportées à une ruche de Registre hors connexion ouverte, utilisez la fonction [**ORSaveHive**](orsavehive.md) pour enregistrer la ruche dans un fichier. (Les modifications ne sont pas conservées, sauf si **ORSaveHive** est appelé.) Après avoir enregistré la ruche, utilisez la fonction [**ORCloseHive**](orclosehive.md) pour fermer la ruche et libérer les ressources qui lui sont associées.

Une ruche de Registre hors connexion est validée uniquement lorsqu’elle est ouverte à l’aide de la fonction [**OROpenHive**](oropenhive.md) . Si la ruche est endommagée, l’opération échoue simplement ; aucune tentative n’est faite pour réparer la ruche. Les vérifications d’accès sur les objets de la ruche ne sont pas effectuées tant que la ruche n’est pas chargée dans un Registre actif avec la fonction [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) .

Les fonctions de Registre hors connexion ne prennent pas en charge les [clés prédéfinies](../sysinfo/predefined-keys.md).

Toutes les chaînes de nom de clé et de valeur transmises aux fonctions de Registre hors connexion doivent être au format Unicode.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de la bibliothèque de Registre hors connexion \_](offline-registry-library-functions.md)
</dt> </dl>

 

 
