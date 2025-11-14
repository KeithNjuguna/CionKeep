# CionKeep
Below is an overview architecture of the Coinkeep mobile application.
I Will use structure to follow and make the architecture matches the application.
// remember to use this on the command prompt
npm install -g expo-cli


mobile/
├── .expo/
├── assets/
│   ├── images/
│   ├── icons/
│   └── fonts/
├── src/
│   ├── api/                    # Supabase client, API helpers
│   │   ├── supabase.js
│   │   ├── apiClient.js
│   │   └── rpcs/               # Postgres RPC wrappers (optional)
│   │
│   ├── components/             # Reusable mobile UI components
│   │   ├── AppHeader.js
│   │   ├── BottomTabBar.js
│   │   ├── DrawerContent.js
│   │   ├── KPICard.js
│   │   ├── ProductCard.js
│   │   ├── TransactionCard.js
│   │   ├── SwipeableListItem.js
│   │   ├── Avatar.js
│   │   ├── IconButton.js
│   │   ├── FloatingActionButton.js
│   │   ├── ModalSheet.js        # bottom sheet modal
│   │   ├── FormField.js
│   │   ├── DatePickerMobile.js
│   │   ├── ImageUploader.js
│   │   └── LoadingPlaceholder.js
│   │
│   ├── navigation/
│   │   ├── AppNavigator.js      # Root navigator (auth gating)
│   │   ├── AuthStack.js
│   │   ├── MainDrawer.js
│   │   ├── HomeTabs.js          # bottom tabs: Dashboard, Inventory, Sales, Reports, More
│   │   └── screens-index.js     # central export mapping of routes
│   │
│   ├── screens/                 # Screen-level components (mapping from your web pages)
│   │   ├── auth/
│   │   │   ├── LoginScreen.js
│   │   │   ├── RegisterScreen.js
│   │   │   ├── ForgotPasswordScreen.js
│   │   │   └── ResetPasswordScreen.js
│   │   │
│   │   ├── dashboard/
│   │   │   ├── DashboardScreen.js
│   │   │   ├── DashboardStats.js
│   │   │   └── DashboardCharts.js
│   │   │
│   │   ├── inventory/
│   │   │   ├── ProductsScreen.js
│   │   │   ├── ProductDetailScreen.js
│   │   │   ├── ProductFormScreen.js
│   │   │   ├── CategoriesScreen.js
│   │   │   ├── StockAdjustmentScreen.js
│   │   │   ├── LowStockScreen.js
│   │   │   └── StockHistoryScreen.js
│   │   │
│   │   ├── sales/
│   │   │   ├── SalesScreen.js
│   │   │   ├── CreateSaleScreen.js
│   │   │   ├── SaleDetailScreen.js
│   │   │   ├── QuotesScreen.js
│   │   │   ├── ReturnsScreen.js
│   │   │   └── InvoiceScreen.js
│   │   │
│   │   ├── purchases/
│   │   │   ├── PurchasesScreen.js
│   │   │   ├── CreatePurchaseScreen.js
│   │   │   ├── ReceiveStockScreen.js
│   │   │   └── PurchaseDetailScreen.js
│   │   │
│   │   ├── customers/
│   │   │   ├── CustomersScreen.js
│   │   │   ├── CustomerFormScreen.js
│   │   │   └── CustomerDetailScreen.js
│   │   │
│   │   ├── suppliers/
│   │   │   ├── SuppliersScreen.js
│   │   │   ├── SupplierFormScreen.js
│   │   │   └── SupplierDetailScreen.js
│   │   │
│   │   ├── financial/
│   │   │   ├── ExpensesScreen.js
│   │   │   ├── ExpenseFormScreen.js
│   │   │   ├── IncomeScreen.js
│   │   │   ├── InvoicesScreen.js
│   │   │   ├── PaymentsScreen.js
│   │   │   └── ReconciliationScreen.js
│   │   │
│   │   ├── reports/
│   │   │   ├── ReportsScreen.js
│   │   │   ├── SalesReportScreen.js
│   │   │   ├── InventoryReportScreen.js
│   │   │   └── ProfitLossScreen.js
│   │   │
│   │   ├── users/
│   │   │   ├── UsersScreen.js
│   │   │   ├── UserFormScreen.js
│   │   │   └── UserDetailScreen.js
│   │   │
│   │   ├── settings/
│   │   │   ├── SettingsScreen.js
│   │   │   ├── CompanySettingsScreen.js
│   │   │   └── NotificationSettingsScreen.js
│   │   │
│   │   └── help/
│   │       ├── HelpScreen.js
│   │       └── SupportScreen.js
│   │
│   ├── contexts/                # Context providers (Auth, Theme, Notifications)
│   │   ├── AuthContext.js
│   │   ├── ThemeContext.js
│   │   └── NotificationContext.js
│   │
│   ├── hooks/                   # Mobile-specific hooks
│   │   ├── useAuth.js
│   │   ├── useProducts.js
│   │   ├── useInfiniteList.js
│   │   └── useOfflineSync.js
│   │
│   ├── services/                # API service layer (maps to your backend services)
│   │   ├── productService.js
│   │   ├── salesService.js
│   │   ├── purchaseService.js
│   │   ├── customerService.js
│   │   ├── supplierService.js
│   │   ├── expenseService.js
│   │   ├── reportService.js
│   │   └── notificationService.js
│   │
│   ├── store/                   # Optional: redux or Zustand for global store
│   │   └── index.js
│   │
│   ├── utils/
│   │   ├── formatters.js
│   │   ├── validators.js
│   │   ├── constants.js
│   │   └── offlineHelpers.js
│   │
│   ├── styles/                  # global/utility styles (NativeWind or StyleSheet)
│   │   └── globals.js
│   │
│   ├── types/                   # types (if using TypeScript)
│   │   └── index.d.ts
│   │
│   ├── App.js                   # App entry (wraps providers)
│   └── index.js                 # Expo entry
│
├── app.json
├── package.json
└── README.md
