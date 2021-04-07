---
title: Comment étendre le schéma
description: Lorsque les classes et/ou les attributs existants ne correspondent pas au type de données que vous souhaitez stocker, vous pouvez étendre le schéma.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- Schéma AD, comment étendre
- Active Directory, utilisation de, schéma
- Active Directory, utiliser, schéma, étendre le schéma, comment étendre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724493"
---
# <a name="how-to-extend-the-schema"></a>Comment étendre le schéma

Lorsque les classes et/ou les attributs existants ne correspondent pas au type de données que vous souhaitez stocker, vous pouvez étendre le schéma. Pour plus d’informations sur le choix de l’extension du schéma, consultez [extension du schéma](extending-the-schema.md). Lorsque vous avez décidé que l’extension de schéma est requise, utilisez la procédure suivante pour étendre le schéma.

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a>Vérifier Active Directory fonctionnalité avant d’appliquer des extensions de schéma

Vérifiez Active Directory fonctionnalité avant de mettre à jour le schéma pour vous assurer que l’extension de schéma continue sans erreur. Au minimum, assurez-vous que tous les contrôleurs de domaine de la forêt sont en ligne et qu’ils effectuent une réplication entrante.

**Pour vérifier Active Directory fonctionnalité avant d’appliquer l’extension de schéma**

1.  Connectez-vous à une station de travail d’administration sur laquelle l’outil de support Windows Repadmin.exe installé.
    > [!Note]  
    > Les outils de support sont situés sur le support d’installation du système d’exploitation dans le \\ dossier Outils de support.

     

2.  Ouvrez une invite de commandes, puis accédez au dossier dans lequel les outils de support Windows sont installés.
3.  À une invite de commandes, tapez ce qui suit puis appuyez sur ENTRÉE :

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    Tous les contrôleurs de domaine doivent afficher la valeur 0 dans la colonne échecs et les deltas les plus importants (qui indiquent le nombre de modifications apportées à la base de données Active Directory depuis la dernière réplication réussie) doivent être inférieurs ou approximativement à la fréquence de réplication du lien de site utilisé par le contrôleur de domaine pour la réplication. La fréquence de réplication par défaut est de 180 minutes.

    Pour plus d’informations sur les étapes supplémentaires que vous pouvez suivre pour vérifier Active Directory fonctionnalités avant d’appliquer l’extension de schéma, consultez [l’article 325379 de la base de connaissances Microsoft](https://support.microsoft.com/kb/325379/en-us).

**Pour étendre le schéma**

1.  Déterminez la méthode de l’extension. Une fois que vous avez soigneusement conçu vos modifications de schéma, l’étape suivante consiste à choisir la méthode à utiliser pour étendre le schéma. Vous pouvez utiliser l’une des méthodes suivantes :
    -   Manuellement, à l’aide des fichiers d’importation. Consultez la documentation [à l’aide de l’outil LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).
        > [!Note]  
        > N’utilisez pas LDIFDE pour importer des fichiers Windows SCH \* . ldf. Ces fichiers sont requis pour étendre le schéma de Active Directory afin d’installer des contrôleurs de domaine qui exécutent une version plus récente de Windows Server que la version exécutée sur le contrôleur de schéma actuel. Lorsque vous avez besoin d’étendre le schéma pour installer un nouveau contrôleur de domaine, utilisez Adprep.exe.

         

    -   Par programmation, à l’aide d’un programme d’installation. Pour plus d’informations, consultez [extension par programmation](programmatic-extension.md)
2.  Activer les modifications de schéma. Pour plus d’informations, consultez [Configuration requise pour l’installation d’une extension de schéma](prerequisites-for-installing-a-schema-extension.md) et [activation des modifications de schéma sur le contrôleur de schéma](enabling-schema-changes-at-the-schema-master.md).
3.  Obtenez un identificateur d’objet (OID) pour vos nouveaux attributs et/ou classes, comme décrit dans [obtention d’un identificateur d’objet](obtaining-an-object-identifier.md).
4.  Créer des attributs et des classes.
5.  Utilisez les spécificateurs d’affichage pour intégrer de nouveaux attributs et classes à l’interface utilisateur, si nécessaire.
6.  Mettez à jour le cache de schéma comme décrit dans [mise à jour du cache de schéma](updating-the-schema-cache.md).
7.  Vérifiez l’extension de schéma à l’aide de LDP.exe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Obtention d’un identificateur d’objet](obtaining-an-object-identifier.md)
</dt> <dt>

[Les nouveaux outils en ligne de commande pour Active Directory dans Windows Server 2003](https://support.microsoft.com/kb/298882)
</dt> <dt>

[Utilisation de l’outil LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))
</dt> <dt>

[Extension du schéma Active Directory](/previous-versions/ms806972(v=msdn.10))
</dt> <dt>

[Restrictions sur l’extension de schéma](restrictions-on-schema-extension.md)
</dt> </dl>

 

 