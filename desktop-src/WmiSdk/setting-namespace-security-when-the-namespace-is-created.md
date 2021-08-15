---
title: Définition de la sécurité pour la création d’espaces de noms
description: Le fichier format MOF (MOF) qui crée un espace de noms peut également définir les descripteurs de sécurité pour l’espace de noms en incluant le qualificateur NamespaceSecuritySDDL avec le descripteur de sécurité au format SDDL (Security Descriptor Definition Language).
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004e1897553ef2ec0bd57067b17d714f6aaf8b17059c1078a2fc0da8a060a40f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315636"
---
# <a name="setting-security-on-namespace-creation"></a>Définition de la sécurité pour la création d’espaces de noms

Le fichier format MOF (MOF) qui crée un espace de noms peut également définir les [*descripteurs de sécurité*](/windows/desktop/SecGloss/s-gly) pour l’espace de noms en incluant le qualificateur **NamespaceSecuritySDDL** avec le descripteur de sécurité au format [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .

Vous pouvez utiliser **NamespaceSecuritySDDL** pour sécuriser n’importe quel espace de noms. Vous pouvez également utiliser ce qualificateur dans un simple fichier MOF pour modifier le descripteur de sécurité sur un espace de noms existant. La chaîne SDDL est traitée par WMI pour établir la sécurité de l’espace de noms, mais elle n’est pas stockée sous forme de chaîne. Si aucun descripteur de sécurité n’est spécifié, la sécurité par défaut est utilisée. Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md).

La procédure suivante définit le descripteur de sécurité pour l’espace de noms *\\ MyNamespace racine* . La chaîne SDDL définit le propriétaire et le groupe sur les utilisateurs authentifiés et spécifie une [*liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) qui est héritée par les espaces de noms enfants. La liste DACL permet à l’utilisateur de lire des données, d’exécuter des méthodes, d’écrire des données dans des classes de fournisseur et d’utiliser l’accès à distance : **WBEM \_ Enable**, **\_ méthode WBEM \_ Execute**, **\_ \_ fournisseur d’écriture WBEM**, **\_ \_ accès à distance WBEM**. Pour plus d’informations, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md).

**Pour définir une liste DACL d’espace de noms**

1.  Créez un fichier format MOF (MOF) ou modifiez votre fichier MOF existant qui définit l’espace de noms pour ajouter le qualificateur **NamespaceSecuritySDDL** à la chaîne SDDL.

    L’exemple de code suivant montre que l’espace de noms à modifier est root \\ MyNamespace et que le fichier est nommé MyNamespace \_ Security. mof.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  Sachez que la chaîne SDDL respecte la casse : les lettres doivent être en majuscules.

    L’exemple de code suivant affiche les lettres « o » et « g » dans la chaîne SDDL en minuscules et génère une erreur Mofcomp.exe.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  Exécutez [**Mofcomp.exe**](mofcomp.md) pour compiler le fichier MOF.

    **c : \\ mofcomp MyNamespace \_ Security. mof**

    En C++, utilisez les méthodes [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

4.  Si votre tentative de définition de la liste DACL d’espace de noms échoue, examinez les messages d’erreur suivants :

    

    | Erreur                           | Description                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | **\_paramètre WBEM E \_ non valide \_** | Il n’y a aucune DACL héritée. Sinon, l’appelant n’a pas respecté la liste DACL ou le SD dans l’espace de noms parent. |
    | **\_accès WBEM \_ E \_ refusé**     | L’appelant n’est pas autorisé à mettre à jour le SDDL dans MOF.                                               |

    

     

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition des descripteurs de sécurité des espaces de noms](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Constantes de droits d’accès à l’espace de noms**](namespace-access-rights-constants.md)
</dt> <dt>

[**Constantes d’indicateur ACE d’espace de noms**](namespace-ace-flag-constants.md)
</dt> <dt>

[Modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
