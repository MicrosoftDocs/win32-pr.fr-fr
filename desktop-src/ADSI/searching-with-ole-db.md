---
title: Recherche avec OLE DB
description: Pour les clients Automation utilisant des ActiveX Data Objects (ADO) et tous les clients non-Automation, ADSI fournit un fournisseur OLE DB qui prend en charge un sous-ensemble d’interfaces de requête OLE DB.
ms.assetid: f4e48b60-82dd-4c39-879b-0bc8f40747d2
ms.tgt_platform: multiple
keywords:
- Recherche avec OLE DB ADSI
- interroge ADSI, en recherchant OLE DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b6b0c056a63174233271b9b059ebffa9d4d841
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730324"
---
# <a name="searching-with-ole-db"></a>Recherche avec OLE DB

Pour les clients Automation utilisant des ActiveX Data Objects (ADO) et tous les clients non-Automation, ADSI fournit un fournisseur OLE DB qui prend en charge un sous-ensemble d’interfaces de requête OLE DB. Le code client qui utilise déjà des interfaces OLE DB pour les requêtes peut utiliser les mêmes interfaces pour interroger les services d’annuaire.

Dans le cadre de l’implémentation de OLE DB, un service d’annuaire est exposé en tant qu’objet de source de données. Les objets de source de données sont des fabriques pour les objets de session et prennent en charge [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) pour se connecter à l’annuaire, [méthode IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) pour créer l’objet de session, [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) pour fournir les données d’authentification à l’espace de noms sous-jacent et fournir la commande de requête et [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) pour enregistrer les données nécessaires pour créer l’objet de source de données dans le service d’annuaire sous-jacent

**Pour exécuter une requête Active Directory à l’aide de OLE DB**

1.  Récupérez l’interface [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) à partir du fournisseur OLE DB. Dans le cas de Active Directory, utilisez l’identificateur de classe **CLSID \_ ADSDSOObject**.
2.  Créez un tableau [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) de données de connexion spécifiant le nom d’utilisateur et le mot de passe.
3.  Interrogez l’interface [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) Récupérée à l’étape 1 pour l’interface [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) .
4.  Appelez la méthode [IDBProperties :: SetProperties](/previous-versions/windows/desktop/ms723049(v=vs.85)) en passant le tableau [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) créé à l’étape 2.
5.  Appelez la méthode [IDBInitialize :: Initialize](/previous-versions/windows/desktop/ms718026(v=vs.85)) pour établir la connexion au fournisseur OLE DB ; Il s’agit du fournisseur Active Directory, dans ce cas.
6.  Interrogez l’interface [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) pour l’interface [méthode IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) .
7.  Appelez la méthode [méthode IDBCreateSession :: CreateSession](/previous-versions/windows/desktop/ms714942(v=vs.85)) en demandant une nouvelle interface de type [IDBCreateCommand](/previous-versions/windows/desktop/ms711625(v=vs.85)).
8.  Appelez la méthode [IDBCreateCommand :: CreateCommand](/previous-versions/windows/desktop/ms709772(v=vs.85)) pour créer une interface [ICommandText](/previous-versions/windows/desktop/ms714914(v=vs.85)) .
9.  Appelez la méthode [ICommandText :: SetCommandText](/previous-versions/windows/desktop/ms709757(v=vs.85)) . Transmettez le dialecte préféré et le texte de la commande de requête réelle dans ce dialecte. **DBGUID \_ LDAPDialect** ou **DBGUID \_ DBSQL** peut être utilisé comme dialecte.
10. Appeler [ICommand :: Execute](/previous-versions/windows/desktop/ms718095(v=vs.85)); une interface [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) est retournée, qui est l’interface du jeu de résultats.
11. Interrogez l’interface [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) pour l’interface [IColumnsInfo](/previous-versions/windows/desktop/ms725401(v=vs.85)) .
12. Appelez la méthode [IColumnsInfo :: GetColumnInfo](/previous-versions/windows/desktop/ms722704(v=vs.85)) pour récupérer des données de colonne sur le jeu de résultats.
13. Remplissez un tableau de structures [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) , en décrivant au fournisseur OLE DB comment exposer les types de données par colonne au code de l’application. Cette étape vous permet de spécifier le TYPE contenu dans une colonne particulière. En outre, les décalages des colonnes, par rapport à la ligne retournée, sont définis ici sur la base d’une colonne par colonne.
14. Interrogez l’interface [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) pour l’interface [IAccessor](/previous-versions/windows/desktop/ms719672(v=vs.85)) .
15. Appelez la méthode [IAccessor :: CreateAccessor](/previous-versions/windows/desktop/ms720969(v=vs.85)) , qui retourne un tableau de handles d’accesseur. Ce tableau est ensuite utilisé pour accéder aux lignes du jeu de résultats.
16. Appelez [IRowset :: GetNextRows](/previous-versions/windows/desktop/ms709827(v=vs.85)) en passant les handles de ligne et le nombre de lignes à récupérer.
17. Appelez [IRowset :: GetData](/previous-versions/windows/desktop/ms716988(v=vs.85)) en passant un handle de ligne, à partir du jeu retourné à l’étape 16. Un pointeur brut vers la ligne est retourné.

Pour plus d’informations sur la syntaxe de filtre de recherche, consultez [syntaxe de filtre de recherche](search-filter-syntax.md).

Pour lire les données de ligne non traitées retournées, utilisez la structure [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) , créée à l’étape 13, calculez les décalages de colonne dans le pointeur de données non traitées retourné à l’étape 17. Lisez la partie État de la colonne pour obtenir un résultat de récupération sur cette colonne.

Pour plus d’informations et pour obtenir un exemple de code qui montre comment rechercher des Active Directory à l’aide du fournisseur d’OLE DB ADSI, consultez [l’exemple de code pour l’utilisation de OLE DB pour rechercher des Active Directory](example-code-for-using-ole-db-to-search-active-directory.md).

 

 