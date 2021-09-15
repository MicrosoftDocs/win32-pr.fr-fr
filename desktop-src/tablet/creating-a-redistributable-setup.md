---
description: pour distribuer une application compatible avec l’écriture manuscrite sur des ordinateurs qui n’exécutent pas Windows Vista ou Windows XP édition Tablet PC 2005 (autrement dit, les ordinateurs exécutant Windows XP, Windows Server 2003 ou Windows 2000), vous devez inclure les modules de fusion nécessaires dans votre installation.
ms.assetid: 97515703-0bf4-4230-ae35-181b48b70c40
title: Création d’une installation redistribuable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ad9b9ec8b10032d4a2bb44cca52e5c2f4178b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294651"
---
# <a name="creating-a-redistributable-setup"></a>Création d’une installation redistribuable

pour distribuer une application compatible avec l’écriture manuscrite sur des ordinateurs qui n’exécutent pas Windows Vista ou Windows XP édition Tablet PC 2005 (autrement dit, les ordinateurs exécutant Windows XP, Windows Server 2003 ou Windows 2000), vous devez inclure les modules de fusion nécessaires dans votre installation.

le module de fusion Mstpcrt. msm comprend tous les fichiers, ressources, entrées de registre et logique d’installation nécessaires à Windows Installer pour installer les fichiers partagés dont les autres plateformes ont besoin pour exécuter des applications non gérées développées pour Tablet PC. Mstpcrt. msm est consommé par les fichiers de Windows Installer (.msi). Pour les applications qui utilisent l’objet [**InkDivider**](inkdivider-class.md) , vous devez également redistribuer InkDiv. msm. Pour les applications qui utilisent des composants managés, vous devez également inclure les fichiers de module de fusion pour ces composants managés.

le tableau suivant décrit les fichiers de module de fusion fournis avec le kit de développement logiciel (SDK) Windows XP Tablet PC Edition.



| Module de fusion redistribuable | Description                                                                                                                    | Fichiers                                                       |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| InkDiv. msm<br/>        | Installe la version non managée de l’objet [**InkDivider**](inkdivider-class.md) .<br/>                                | InkDiv.dll<br/>                                       |
| Mstpcrt. msm<br/>       | Installe les composants non gérés de la plate-forme Tablet PC version 1,0.<br/>                                            | Gdiplus.dll, InkEd.dll, Tpcps.dll, Wisptis.exe<br/>   |
| Msvcp60. msm<br/>       | installe les composants du runtime Microsoft Visual C++.<br/>                                                            | Msvcp60.dll<br/>                                      |
| Msvcrt. msm<br/>        | Installe les composants du runtime Microsoft Visual C.<br/>                                                              | Msvcrt.dll<br/>                                       |
| Tpcman17. msm<br/>      | Installe les composants managés du composant d’exécution de la plateforme Tablet PC. Requiert l’installation du fichier mstpcrt. msm.<br/> | Microsoft.Ink.dll, Microsoft.Ink.resources.dll<br/>   |
| iaCOM. msm<br/>         | Installe les composants d’Automation de l’API InkAnalysis.<br/>                                                          | IACom.dll<br/>                                        |
| IACore. msm<br/>        | Installe les composants de la classe de base de l’API InkAnalysis.<br/>                                                          | IACore.dll<br/> IALoader.dll<br/>               |
| IAWinFrm. msm<br/>      | Installe les composants de la bibliothèque managée de l’API InkAnalysis.<br/>                                                     | Microsoft.Ink.Analysis.dll<br/>                       |
| IAWinFX. msm<br/>       | installe les composants Windows Presentation Foundation de l’API InkAnalysis.<br/>                                     | IAWinFX.dll<br/>                                      |
| Journal. msm<br/>       | Installe les composants du lecteur de journal.<br/>                                                                             | Journal.dll<br/> Microsoft.ink.journal.dll<br/> |
| rtscom. msm<br/>        | Installe les composants d’Automation de l’espace de noms StylusInput.<br/>                                                    | Rtscom.dll<br/>                                       |



 

> [!Note]  
> pour utiliser les fonctionnalités de la .NET Framework Microsoft qui est incluse dans les modules de fusion pour les composants gérés, vous devez avoir installé le Service Pack 2 de l’infrastructure sur l’ordinateur cible.

 

## <a name="reduced-feature-set"></a>Ensemble de fonctionnalités réduit

Les applications prenant en charge l’encre considèrent les événements de souris comme des mouvements de stylet pour simuler l’utilisation d’un stylet. Les utilisateurs peuvent ajouter de l’encre, effacer l’encre et enregistrer les documents manuscrits. toutefois, la reconnaissance et les gestes ne sont pas disponibles pour les utilisateurs autres que ceux qui exécutent Windows XP édition Tablet PC.

Mstpcrt. msm n’inclut pas Windows Journal ou le panneau de saisie Tablet pc.

l’objet [**PenInputPanel**](peninputpanel-class.md) ne fonctionne pas sur les systèmes d’exploitation autres que Windows XP édition Tablet PC.

## <a name="deployment"></a>Déploiement

> [!Note]  
> Si votre application utilise du code managé, vous devez également déployer le Framework. L’infrastructure doit être installée avant l’installation de vos assemblys gérés par Tablet PC.

 

pour inclure Mstpcrt. msm dans un projet d’installation Microsoft Visual Studio .net :

1.  Dans le Explorateur de solutions, sélectionnez votre projet d’installation.
2.  dans le menu Project, cliquez sur **ajouter**, puis sur **Module de fusion**.
    > [!Note]  
    > Vous pouvez également accéder à la boîte de dialogue **Ajouter des modules** en cliquant avec le bouton droit sur le nom du projet d’installation dans le Explorateur de solutions, en cliquant sur **Ajouter**, puis en sélectionnant **module de fusion**.

     

3.  Dans la boîte de dialogue **Ajouter des modules** , accédez à **mstpcrt. msm** et sélectionnez-le.
4.  Cliquez sur **Ouvrir**.

Mstpcrt. msm est ajouté à votre projet d’installation et s’affiche dans la fenêtre Explorateur de solutions.

Windows Le programme d’installation ajoute les fichiers contenus dans le module de fusion dans le dossier Program Files. Pour utiliser ces fichiers, les utilisateurs finaux doivent avoir ouvert une session avec un compte qui a accès au dossier Program Files.

> [!Note]  
> Vous devez ajouter des actions action [SelfRegModules](../msi/selfregmodules-action.md) et [action SelfUnregModules](../msi/selfunregmodules-action.md) à la séquence d’installation. Les actions [action MsiPublishAssemblies](../msi/msipublishassemblies-action.md) et [action MsiUnpublishAssemblies](/windows/desktop/Msi/msiunpublishassemblies-action) reçoivent leur ordre dans la séquence d’installation à partir de ces actions.

 

 

