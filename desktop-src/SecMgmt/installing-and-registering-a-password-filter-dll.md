---
description: la DLL de filtre de mot de passe Windows, Passfilt.dll, s’exécute dans le contexte de sécurité du compte système local et vous aide à filtrer les mots de passe de compte local ou de domaine.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Installation et inscription d’une DLL de filtre de mot de passe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2e9f93630dc6bdaa5dbcc7e665a6b1cebff0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324738"
---
# <a name="installing-and-registering-a-password-filter-dll"></a>Installation et inscription d’une DLL de filtre de mot de passe

vous pouvez utiliser le filtre de mot de passe Windows pour filtrer les mots de passe de compte local ou de domaine. Pour utiliser le filtre de mot de passe pour les comptes de domaine, installez et inscrivez la DLL sur chaque contrôleur de domaine du domaine.

Procédez comme suit pour installer votre filtre de mot de passe. Vous pouvez effectuer ces étapes manuellement, ou vous pouvez écrire un programme d’installation pour effectuer ces étapes. Pour effectuer ces étapes, vous devez être administrateur ou appartenir au groupe administrateurs.

**pour installer et inscrire une DLL de filtre de mot de passe Windows**

1.  copiez la DLL dans le répertoire d’installation de Windows sur le contrôleur de domaine ou l’ordinateur local. sur les installations standard, le dossier par défaut est \\ Windows \\ System32. Veillez à créer une DLL de filtre de mots de passe 32 bits pour les ordinateurs 32 bits et une DLL de filtre de mot de passe 64 bits pour les ordinateurs 64 bits, puis copiez-les à l’emplacement approprié.
2.  Pour inscrire le filtre de mot de passe, mettez à jour la clé de Registre système suivante :

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    Si la valeur des **packages de notifications** de type *REG_MULTI_SZ* existe, ajoutez le nom de votre dll aux données de la valeur existante. Ne remplacez pas les valeurs existantes et n’incluez pas l’extension .dll.

    Si la valeur des **packages de notifications** n’existe pas, créez-la, donnez-lui le type de *REG_MULTI_SZ* , puis spécifiez le nom de la dll pour les données de la valeur. N’incluez pas l’extension de .dll.

    La valeur des **packages de notifications** peut ajouter plusieurs packages.

3.  Recherchez le paramètre de complexité du mot de passe.

    Dans le panneau de configuration, cliquez sur **performances et maintenance**, sur **Outils d’administration**, double-cliquez sur **stratégie de sécurité locale**, sur **stratégies de comptes**, puis sur **stratégie de mot de passe**.

4.  pour appliquer le filtre de mot de passe Windows par défaut et le filtre de mot de passe personnalisé, assurez-vous que le paramètre de stratégie les **mots de passe doivent respecter les exigences de complexité** est activé. Dans le cas contraire, désactivez le paramètre de stratégie les **mots de passe doivent respecter des exigences de complexité** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Considérations sur la programmation du filtre de mot de passe](password-filter-programming-considerations.md)
</dt> <dt>

[Mise en œuvre des mots de passe forts et Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[Fonctions de filtre de mot de passe](management-functions.md)
</dt> </dl>

 

 



